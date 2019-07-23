# ejerciciosRutaTresSinArrays
Ejercicios propuestos para Ruta 3

Scanner teclado = new Scanner(System.in);

        int numeroDeFactura = 0;
        int promociones = 0;
        int facturaMayor = 0;

        float importe, dinero, vuelto, suma = 0, ventasEfectivo = 0,
                ventasTarjeta = 0, ventaMayor = 0;

        String metodoDePago;

        for (int i = 0; i < 10; i++) {

            System.out.print("NÚMERO DE FACTURA: ");
            numeroDeFactura = teclado.nextInt();

            System.out.print("IMPORTE: $");
            importe = teclado.nextFloat();
            suma = suma + importe;

            if (importe > ventaMayor) {
                ventaMayor = importe;
                facturaMayor = numeroDeFactura;
            }

            System.out.println("METODO DE PAGO \nEfectivo [E] \nTarjeta [T]");
            System.out.print("... ");
            metodoDePago = teclado.next();

            if (metodoDePago.equalsIgnoreCase("E")) {

                ventasEfectivo++;

                System.out.print("DINERO: $");
                dinero = teclado.nextFloat();

                if (importe >= 1000 && dinero >= importe) {

                    promociones++;

                    float porcentaje, resultado;

                    System.out.print("10% DE DESCUENTO");
                    System.out.println("");

                    porcentaje = (10 * importe) / 100;
                    resultado = importe - porcentaje;

                    System.out.print("DEBE PAGAR: $" + resultado);
                    System.out.println("");

                    vuelto = dinero - resultado;

                    System.out.print("SU VUELTO ES: $" + vuelto);
                    System.out.println("");

                    System.out.print("SE AHORRÓ: $" + porcentaje);
                    System.out.println("");

                } else {

                    if (dinero >= importe) {

                        System.out.print("DEBE PAGAR: $" + importe);
                        System.out.println("");

                        vuelto = dinero - importe;

                        System.out.print("SU VUELTO ES: $" + vuelto);
                        System.out.println("");

                    } else {

                        System.out.print("DINERO INSUFICIENTE");
                        System.out.println("");

                    }

                }

            } else if (metodoDePago.equalsIgnoreCase("T")) {

                ventasTarjeta++;

                System.out.print("DEBE PAGAR: $" + importe);
                System.out.println("");

            } else {

                System.out.print("MÉTODO DE PAGO INCORRECTO");
                System.out.println("");

            }

        }

        int porcentajeEfectivo = (int) ((10 - ventasTarjeta) / 10 * 100);
        int porcentajeTarjeta = (int) ((10 - ventasEfectivo) / 10 * 100);

        System.out.print("Promociones: " + promociones);
        System.out.println("");
        System.out.print("Ventas en efectivo: " + porcentajeEfectivo + "%");
        System.out.println("");
        System.out.print("Ventas con tarjeta: " + porcentajeTarjeta + "%");
        System.out.println("");
        System.out.print("Mayor venta: $" + ventaMayor + " - N° de factura: " + facturaMayor);
        System.out.println("");
        System.out.print("Total facturado: $" + suma);
        System.out.println("");
