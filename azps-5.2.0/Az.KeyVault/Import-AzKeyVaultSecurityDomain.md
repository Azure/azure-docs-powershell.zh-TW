---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282012"
---
# <span data-ttu-id="a5a67-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="a5a67-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="a5a67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5a67-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a67-103">將先前匯出的安全網域資料匯入到受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a5a67-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="a5a67-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5a67-104">SYNTAX</span></span>

### <span data-ttu-id="a5a67-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a5a67-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5a67-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a67-107">說明</span><span class="sxs-lookup"><span data-stu-id="a5a67-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a67-108">這個 Cmdlet 會將先前匯出的安全網域資料匯入受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a5a67-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="a5a67-109">示例</span><span class="sxs-lookup"><span data-stu-id="a5a67-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a67-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a5a67-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="a5a67-111">首先，需要提供金鑰來解密安全網域資料。</span><span class="sxs-lookup"><span data-stu-id="a5a67-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="a5a67-112">接著，[匯 **入-AzKeyVaultSecurityDomain** ] 命令會使用這些金鑰，將先前備份的安全性網域資料還原到受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a5a67-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="a5a67-113">參數</span><span class="sxs-lookup"><span data-stu-id="a5a67-113">PARAMETERS</span></span>

### <span data-ttu-id="a5a67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a67-114">-DefaultProfile</span></span>
<span data-ttu-id="a5a67-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5a67-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a67-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a67-116">-InputObject</span></span>
<span data-ttu-id="a5a67-117">代表受管理的 HSM 的物件。</span><span class="sxs-lookup"><span data-stu-id="a5a67-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a67-118">-按鍵</span><span class="sxs-lookup"><span data-stu-id="a5a67-118">-Keys</span></span>
<span data-ttu-id="a5a67-119">有關用來解密安全網域資料之金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="a5a67-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="a5a67-120">請參閱如何構造它的範例。</span><span class="sxs-lookup"><span data-stu-id="a5a67-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a67-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5a67-121">-Name</span></span>
<span data-ttu-id="a5a67-122">受管理的 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a67-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a67-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a67-123">-PassThru</span></span>
<span data-ttu-id="a5a67-124">在指定時，會在 Cmdlet 成功時傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="a5a67-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a67-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="a5a67-125">-SecurityDomainPath</span></span>
<span data-ttu-id="a5a67-126">指定加密安全網域資料的路徑。</span><span class="sxs-lookup"><span data-stu-id="a5a67-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a67-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a5a67-127">-Confirm</span></span>
<span data-ttu-id="a5a67-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5a67-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a67-129">-WhatIf</span></span>
<span data-ttu-id="a5a67-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5a67-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a67-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5a67-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a67-132">CommonParameters</span></span>
<span data-ttu-id="a5a67-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5a67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a67-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5a67-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a67-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a5a67-135">INPUTS</span></span>

### <span data-ttu-id="a5a67-136">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a5a67-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="a5a67-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a5a67-137">OUTPUTS</span></span>

### <span data-ttu-id="a5a67-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a5a67-138">System.Boolean</span></span>

## <span data-ttu-id="a5a67-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a5a67-139">NOTES</span></span>

## <span data-ttu-id="a5a67-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5a67-140">RELATED LINKS</span></span>
