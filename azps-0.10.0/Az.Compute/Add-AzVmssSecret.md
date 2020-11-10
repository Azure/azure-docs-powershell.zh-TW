---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 908810f658cdd4083bd24356eaab4e52d4dd5158
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395113"
---
# <span data-ttu-id="fece5-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="fece5-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="fece5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fece5-102">SYNOPSIS</span></span>
<span data-ttu-id="fece5-103">將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fece5-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="fece5-104">句法</span><span class="sxs-lookup"><span data-stu-id="fece5-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fece5-105">說明</span><span class="sxs-lookup"><span data-stu-id="fece5-105">DESCRIPTION</span></span>
<span data-ttu-id="fece5-106">**AzVmssSecret** Cmdlet 會將機密新增至虛擬電腦比例集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="fece5-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fece5-107">密碼必須儲存在 Azure 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="fece5-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="fece5-108">如需與主要保存庫相關的詳細資訊，請參閱 [何謂 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="fece5-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="fece5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="fece5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="fece5-110">如需有關 Cmdlet 的詳細資訊，請參閱 [Azure 金鑰保存庫 Cmdlet](/powershell/module/az.keyvault) 或 [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fece5-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="fece5-111">示例</span><span class="sxs-lookup"><span data-stu-id="fece5-111">EXAMPLES</span></span>

### <span data-ttu-id="fece5-112">範例1：將機密新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="fece5-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="fece5-113">這個範例會將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fece5-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="fece5-114">第一個命令使用 Get-AzKeyVault Cmdlet 從名為 ContosoVault 的保存庫取得 vault 密碼，並將結果儲存在名為 $Vault 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fece5-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="fece5-115">第二個命令使用 **新的 AzVmssVaultCertificateConfig** Cmdlet，以使用指定的憑證儲存在名為 certificate 的憑證，並將結果儲存在名為 $CertConfig 的變數中，以建立主要 Vault 憑證配置。</span><span class="sxs-lookup"><span data-stu-id="fece5-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="fece5-116">第三個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fece5-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="fece5-117">第四個命令使用 vault 機密，在 VMSS 中使用 [金鑰資源識別碼] 和 [$CertConfig 變數] $Vault 中儲存的保存庫證書，來將機密新增至。</span><span class="sxs-lookup"><span data-stu-id="fece5-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="fece5-118">參數</span><span class="sxs-lookup"><span data-stu-id="fece5-118">PARAMETERS</span></span>

### <span data-ttu-id="fece5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fece5-119">-DefaultProfile</span></span>
<span data-ttu-id="fece5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fece5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fece5-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fece5-121">-SourceVaultId</span></span>
<span data-ttu-id="fece5-122">指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fece5-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="fece5-123">此值也會充當新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="fece5-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="fece5-124">這表示當您從相同的金鑰保存庫新增多個憑證時，您可以使用相同的 *SourceVaultId* 參數值。</span><span class="sxs-lookup"><span data-stu-id="fece5-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="fece5-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fece5-125">-VaultCertificate</span></span>
<span data-ttu-id="fece5-126">指定包含憑證 URL 與憑證名稱的保存庫 **憑證** 物件。</span><span class="sxs-lookup"><span data-stu-id="fece5-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="fece5-127">您可以使用 [新的-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="fece5-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="fece5-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fece5-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fece5-129">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="fece5-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="fece5-130">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="fece5-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="fece5-131">-確認</span><span class="sxs-lookup"><span data-stu-id="fece5-131">-Confirm</span></span>
<span data-ttu-id="fece5-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fece5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fece5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fece5-133">-WhatIf</span></span>
<span data-ttu-id="fece5-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fece5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fece5-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fece5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fece5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fece5-136">CommonParameters</span></span>
<span data-ttu-id="fece5-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fece5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fece5-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fece5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fece5-139">輸入</span><span class="sxs-lookup"><span data-stu-id="fece5-139">INPUTS</span></span>

### <span data-ttu-id="fece5-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fece5-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="fece5-141">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fece5-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="fece5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="fece5-142">OUTPUTS</span></span>

### <span data-ttu-id="fece5-143">所有</span><span class="sxs-lookup"><span data-stu-id="fece5-143">None</span></span>
<span data-ttu-id="fece5-144">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fece5-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fece5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fece5-145">NOTES</span></span>

## <span data-ttu-id="fece5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="fece5-146">RELATED LINKS</span></span>

[<span data-ttu-id="fece5-147">新-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="fece5-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="fece5-148">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fece5-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
