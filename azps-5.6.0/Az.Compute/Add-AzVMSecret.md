---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904538"
---
# Add-AzVMSecret

## 簡介
為虛擬機器新增一個秘訣。

## 語法

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-Az VIRTUALSecret** Cmdlet 為虛擬機器新增了一個秘訣。
此值可讓您新增憑證至虛擬機器。
機密必須儲存在金鑰保存庫中。
有關金鑰庫的資訊，請參閱什麼是[Azure 金鑰庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
有關 Cmdlet 的資訊，請參閱 [Azure 金鑰庫 Cmdlet 或](/powershell/module/az.keyvault) [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet。

## 例子

### 範例 1：新增密碼至虛擬機器
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

第一個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
第二個命令會使用 Get-Credential Cmdlet 建立認證物件，然後將結果儲存在$Credential變數中。
命令會提示您輸入使用者名稱和密碼。
如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。
第三個命令使用 **Set-Az VIRTUALOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。
第四個命令會指派來源庫識別碼給$SourceVaultId變數，供日後使用。
命令會假設$SubscriptionId變數有適當的值。
第五個命令會指派值給 $CertificateStore 01 變數，供日後使用。
第六個命令會指派憑證存放區 URL。
第七個命令會為儲存在 $VirtualMachine 中的虛擬機器新增一個$VirtualMachine。
SourceVaultId 參數會指定 Key Vault。
命令會指定憑證存放區的名稱，以及憑證的 URL。
您可以重複執行 **Add-AzMSSECret，** 為其他憑證新增秘訣。

## 參數

### -CertificateStore
指定執行 Windows 作業系統之虛擬機器上的憑證存放區名稱。
此 Cmdlet 會將憑證新增到此參數指定的儲存區。
您僅能針對執行 Windows 作業系統的虛擬機器指定此參數。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
指定指向包含憑證之 Key Vault 機密的 URL。
憑證是下列 JavaScript 物件標記法 (JSON) 物件的 Base64 編碼，其編碼方式為 UTF-8：{ "data"： " \<Base64-encoded-file\> \<file-format\> password"： \<pfx-file-password\> " " } 目前，dataType 僅接受 .pfx 檔案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
指定金鑰庫的資源識別碼，其中包含您可以新加入虛擬機器的憑證。
此值也做為新增多個憑證的金鑰。
這表示當您從同一個金鑰庫新增多個憑證時，可以使用相同的 *SourceVaultId* 值。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 修改的虛擬機器物件。
若要取得虛擬機器物件，請使用[Get-Az%。CMdlet。](./Get-AzVM.md)
您可以使用 [New-AzMSConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### System.String

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Get-AzMS](./Get-AzVM.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)

[Set-AzEVOperatingSystem](./Set-AzVMOperatingSystem.md)
