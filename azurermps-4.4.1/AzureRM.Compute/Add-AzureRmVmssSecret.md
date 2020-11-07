---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 26811c16f2946b1605c2d3052dc7aca481917d11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625229"
---
# <span data-ttu-id="839d2-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="839d2-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="839d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="839d2-102">SYNOPSIS</span></span>
<span data-ttu-id="839d2-103">將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="839d2-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="839d2-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="839d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="839d2-105">DESCRIPTION</span></span>
<span data-ttu-id="839d2-106">**AzureRmVmssSecret** Cmdlet 會將機密新增至虛擬電腦比例集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="839d2-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="839d2-107">密碼必須儲存在 Azure 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="839d2-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="839d2-108">如需與主要保存庫相關的詳細資訊，請參閱 [何謂 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="839d2-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="839d2-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="839d2-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="839d2-110">如需有關 Cmdlet 的詳細資訊， [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx)請參閱 https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 開發人員網路庫或[AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) Cmdlet 中的 Azure 金鑰保存庫 Cmdlet (。</span><span class="sxs-lookup"><span data-stu-id="839d2-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="839d2-111">示例</span><span class="sxs-lookup"><span data-stu-id="839d2-111">EXAMPLES</span></span>

### <span data-ttu-id="839d2-112">範例1：將機密新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="839d2-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="839d2-113">這個範例會將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="839d2-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="839d2-114">第一個命令使用 Get-AzureRmKeyVault Cmdlet 從名為 ContosoVault 的保存庫取得 vault 密碼，並將結果儲存在名為 $Vault 的變數中。</span><span class="sxs-lookup"><span data-stu-id="839d2-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="839d2-115">第二個命令使用 **新的 AzureRmVmssVaultCertificateConfig** Cmdlet，以使用指定的憑證儲存在名為 certificate 的憑證，並將結果儲存在名為 $CertConfig 的變數中，以建立主要 Vault 憑證配置。</span><span class="sxs-lookup"><span data-stu-id="839d2-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="839d2-116">第三個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="839d2-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="839d2-117">第四個命令使用 vault 機密，在 VMSS 中使用 [金鑰資源識別碼] 和 [$CertConfig 變數] $Vault 中儲存的保存庫證書，來將機密新增至。</span><span class="sxs-lookup"><span data-stu-id="839d2-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="839d2-118">參數</span><span class="sxs-lookup"><span data-stu-id="839d2-118">PARAMETERS</span></span>

### <span data-ttu-id="839d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839d2-119">-DefaultProfile</span></span>
<span data-ttu-id="839d2-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="839d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="839d2-121">-SourceVaultId</span></span>
<span data-ttu-id="839d2-122">指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="839d2-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="839d2-123">此值也會充當新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="839d2-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="839d2-124">這表示當您從相同的金鑰保存庫新增多個憑證時，您可以使用相同的 *SourceVaultId* 參數值。</span><span class="sxs-lookup"><span data-stu-id="839d2-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="839d2-125">-VaultCertificate</span></span>
<span data-ttu-id="839d2-126">指定包含憑證 URL 與憑證名稱的保存庫 **憑證** 物件。</span><span class="sxs-lookup"><span data-stu-id="839d2-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="839d2-127">您可以使用 [新的-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="839d2-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="839d2-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="839d2-129">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="839d2-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="839d2-130">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="839d2-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-131">-確認</span><span class="sxs-lookup"><span data-stu-id="839d2-131">-Confirm</span></span>
<span data-ttu-id="839d2-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="839d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839d2-133">-WhatIf</span></span>
<span data-ttu-id="839d2-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="839d2-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="839d2-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="839d2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839d2-136">CommonParameters</span></span>
<span data-ttu-id="839d2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="839d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839d2-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="839d2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839d2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="839d2-139">INPUTS</span></span>

### <span data-ttu-id="839d2-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="839d2-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="839d2-141">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="839d2-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="839d2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="839d2-142">OUTPUTS</span></span>

### <span data-ttu-id="839d2-143">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="839d2-143">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="839d2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="839d2-144">NOTES</span></span>

## <span data-ttu-id="839d2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="839d2-145">RELATED LINKS</span></span>

[<span data-ttu-id="839d2-146">新-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="839d2-146">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="839d2-147">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="839d2-147">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
