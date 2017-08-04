# KCustomizer
KCustomizer is WordPress Customizer Utility Class to help create customizer panel, section and controller. Most of time we are repeating code so this class hleps to DRY code. 

## How yo use ?
* Include class file in your funciton.php or somewhere in your theme
* initialize class object like `$customizer = new KCustomizer($wp_customize);`
* create your fields by initalizing array bellow is sample code
<pre>
$default = array(
                'panel' => array(
                    'id'            => "panel13",
                    'label'         => "Panel33",
                    "desc"          => "",
                    "priority"      => 1
                ),
                "sections" => array(
                    array(
                    'section' => array(
                            'id'        => "section_2",
                            'label'     => "Section 2",
                            'priority'  => 2
                        ),
                        'fields' => array(
                            array(
                                // for settigns
                                'default'   => "chitrajan",
                                'callback'  => null,
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "chitrajnan_text",
                                'type'  => 'text',
                                'label' => "Field Label1",
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-2",
                                'type'  => 'text',
                                'label' => "Field Label2"
                            )
                        )
                    ),
                    array(
                    'section' => array(
                            'id'        => "section_2_2",
                            'label'     => "Section 22",
                            'priority'  => 2
                        ),
                        'fields' => array(
                            array(
                                // for settigns
                                'default'   => "chitrajan",
                                'callback'  => null,
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "chitrajnan_text",
                                'type'  => 'text',
                                'label' => "Field Label12",
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-22",
                                'type'  => 'text',
                                'label' => "Field Label22"
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-224",
                                'type'  => 'image',
                                'label' => "Field Label224"
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-2244",
                                'type'  => 'color',
                                'label' => "Field Label2244"
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-22444",
                                'type'  => 'file',
                                'label' => "Field Label22444"
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-22444",
                                'type'  => 'category',
                                'label' => "Field Label22444"
                            ),
                            array(
                                // for settigns
                                'default'   => "kishor",
                                'transport' => 'postMessage',
                                //for control
                                'id'    => "fields_id-223444",
                                'type'  => 'dropdown-pages',
                                'label' => "Field Label232444"
                            )
                        )
                    )
                    
                )
            );
       </pre>
* now call the prepare fucntion to clreate fields `$customizer->prepare( $default ); `

## How to create fields without Panel ?
* Remove panel key from the array it's works as you like

## Can we create single section ?
* Yah sure, you can create as previous or pass single section. Example :
<pre>
$default = array(
                'panel' => array(
                    'id'            => "panel1",
                    'label'         => "Panel",
                    "desc"          => "",
                    "priority"      => 1
                ),
                'section' => array(
                    'id'        => "section_1",
                    'label'     => "Section",
                    'priority'  => 1,
                    'panel' => '',
                ),
                'fields' => array(
                    array(
                        // for settigns
                        'default'   => null,
                        'callback'  => null,
                        'transport' => 'postMessage',
                        //for control
                        'id'    => "fields_id-2",
                        'type'  => 'file',
                        'label' => "Field Label",
                    ),
                    array(
                        // for settigns
                        'default'   => null,
                        'transport' => 'postMessage',
                        //for control
                        'id'    => "good man",
                        'type'  => 'textarea',
                        'label' => "Field Label23"
                    ),
                    array(
                        'default'=> true,
                        'transport' => "refresh",
                        'id'    => "radio_test44",
                        "type"  => "file",
                        "label" => "Radio Test"
                    )
                )
            );
</pre>
