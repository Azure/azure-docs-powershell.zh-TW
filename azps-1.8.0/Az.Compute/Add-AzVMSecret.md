---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: b6d5d7b68726d1e5121491a6b4c5b371a9ec7cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788585"
---
# Add-AzVMSecret

## 摘要
將機密新增至虛擬機器。

## 句法

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzVMSecret** Cmdlet 會將機密新增至虛擬機器。
此值可讓您將憑證新增至虛擬機器。
密碼必須儲存在金鑰保存庫中。
如需有關主要保存庫的詳細資訊，請參閱 [什麼是 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)。
如需有關 Cmdlet 的詳細資訊，請參閱 Microsoft 開發人員網路庫或[AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet 中的[Azure 金鑰保存庫 Cmdlet](https://msdn.microsoft.com/library/azure/dn868052.aspx) 。

## 示例

### 範例1：將密碼新增至虛擬機器
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。
該命令會將名稱和大小指派給虛擬機器。
第二個命令會使用 Get-Credential Cmdlet 來建立認證物件，然後將結果儲存在 $Credential 變數中。
該命令會提示您輸入使用者名稱和密碼。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。
第三個命令使用 **AzVMOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。
第四個命令會將來源電子倉庫識別碼指派給 $SourceVaultId 變數，以供日後使用。
此命令假設 $SubscriptionId 變數具有適當的值。
第五個命令會將值賦給 $CertificateStore 01 變數，以供日後使用。
第六個命令會指派憑證存放區的 URL。
第七個命令會將機密新增至儲存在 $VirtualMachine 的虛擬機器中。
SourceVaultId 參數會指定金鑰保存庫。
此命令會指定憑證存放區的名稱和憑證的 URL。
您可以重複執行 **附加程式 AzVMSecret** ，以新增其他憑證的機密資訊。

## 參數

### -CertificateStore
指定執行 Windows 作業系統的虛擬機器上的憑證存放區名稱。
這個 Cmdlet 會將憑證新增到此參數指定的存放區。
您只能針對執行 Windows 作業系統的虛擬機器指定此參數。

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
指定指向包含憑證之主要 Vault 機密的 URL。
憑證是下列 JavaScript 物件)  (符號的 Base64 編碼，該物件是以 UTF-8 所編碼： {"data"： " \< Base64-編碼-檔案 \> "，"dataType"： " \< 檔案格式 \> "，"密碼"： " \< pfx-檔案密碼 \> "} 目前只有 dataType 可接受 .pfx 檔案。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。
此值也會充當新增多個憑證的金鑰。
這表示當您從相同的金鑰保存庫新增多個憑證時，可以使用與 *SourceVaultId* 相同的值。

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
若要取得虛擬機器物件，請使用 [AzVM](./Get-AzVM.md) Cmdlet。
您可以使用 [新的 AzVMConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSVirtualMachine 中的 [計算] 命令

### System.object

## 輸出

### PSVirtualMachine 中的 [計算] 命令

## 筆記

## 相關連結

[AzVM](./Get-AzVM.md)

[新-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
