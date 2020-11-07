---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: c5bc6295db0346b12f42093a2e03f8de137a4146
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966341"
---
# <span data-ttu-id="9a775-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="9a775-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="9a775-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a775-102">SYNOPSIS</span></span>
<span data-ttu-id="9a775-103">將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="9a775-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="9a775-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a775-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a775-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a775-105">DESCRIPTION</span></span>
<span data-ttu-id="9a775-106">**AzVmssSecret** Cmdlet 會將機密新增至虛擬電腦比例集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="9a775-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9a775-107">密碼必須儲存在 Azure 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="9a775-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="9a775-108">如需與主要保存庫相關的詳細資訊，請參閱 [何謂 Azure 金鑰保存庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="9a775-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="9a775-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="9a775-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="9a775-110">如需有關 Cmdlet 的詳細資訊， [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx)請參閱 https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 開發人員網路庫或[AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet 中的 Azure 金鑰保存庫 Cmdlet (。</span><span class="sxs-lookup"><span data-stu-id="9a775-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="9a775-111">示例</span><span class="sxs-lookup"><span data-stu-id="9a775-111">EXAMPLES</span></span>

### <span data-ttu-id="9a775-112">範例1：將機密新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="9a775-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="9a775-113">這個範例會將機密新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="9a775-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="9a775-114">第一個命令使用 Get-AzKeyVault Cmdlet 從名為 ContosoVault 的保存庫取得 vault 密碼，並將結果儲存在名為 $Vault 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9a775-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="9a775-115">第二個命令使用 **新的 AzVmssVaultCertificateConfig** Cmdlet，以使用指定的憑證儲存在名為 certificate 的憑證，並將結果儲存在名為 $CertConfig 的變數中，以建立主要 Vault 憑證配置。</span><span class="sxs-lookup"><span data-stu-id="9a775-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="9a775-116">第三個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9a775-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="9a775-117">第四個命令使用 vault 機密，在 VMSS 中使用 [金鑰資源識別碼] 和 [$CertConfig 變數] $Vault 中儲存的保存庫證書，來將機密新增至。</span><span class="sxs-lookup"><span data-stu-id="9a775-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="9a775-118">參數</span><span class="sxs-lookup"><span data-stu-id="9a775-118">PARAMETERS</span></span>

### <span data-ttu-id="9a775-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a775-119">-DefaultProfile</span></span>
<span data-ttu-id="9a775-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a775-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a775-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9a775-121">-SourceVaultId</span></span>
<span data-ttu-id="9a775-122">指定包含您可以新增至虛擬機器之憑證的主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a775-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="9a775-123">此值也會充當新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="9a775-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="9a775-124">這表示當您從相同的金鑰保存庫新增多個憑證時，您可以使用相同的 *SourceVaultId* 參數值。</span><span class="sxs-lookup"><span data-stu-id="9a775-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a775-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9a775-125">-VaultCertificate</span></span>
<span data-ttu-id="9a775-126">指定包含憑證 URL 與憑證名稱的保存庫 **憑證** 物件。</span><span class="sxs-lookup"><span data-stu-id="9a775-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="9a775-127">您可以使用 [新的-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="9a775-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a775-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a775-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a775-129">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="9a775-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="9a775-130">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="9a775-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a775-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9a775-131">-Confirm</span></span>
<span data-ttu-id="9a775-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a775-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a775-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a775-133">-WhatIf</span></span>
<span data-ttu-id="9a775-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a775-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a775-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a775-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a775-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a775-136">CommonParameters</span></span>
<span data-ttu-id="9a775-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a775-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a775-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a775-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a775-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9a775-139">INPUTS</span></span>

### <span data-ttu-id="9a775-140">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9a775-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9a775-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9a775-141">System.String</span></span>

### <span data-ttu-id="9a775-142">VaultCertificate [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="9a775-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="9a775-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9a775-143">OUTPUTS</span></span>

### <span data-ttu-id="9a775-144">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9a775-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9a775-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9a775-145">NOTES</span></span>

## <span data-ttu-id="9a775-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a775-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a775-147">新-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="9a775-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="9a775-148">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9a775-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
