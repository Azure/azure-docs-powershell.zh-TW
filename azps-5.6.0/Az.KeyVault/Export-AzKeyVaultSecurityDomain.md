---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 6373ddf37e95c8451afbe8a24b6bade2ca5d3bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912830"
---
# <span data-ttu-id="b5f96-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="b5f96-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="b5f96-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5f96-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f96-103">匯出受管理 HSM 的安全性網域資料。</span><span class="sxs-lookup"><span data-stu-id="b5f96-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="b5f96-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5f96-104">SYNTAX</span></span>

### <span data-ttu-id="b5f96-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5f96-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5f96-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5f96-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f96-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5f96-107">DESCRIPTION</span></span>
<span data-ttu-id="b5f96-108">匯出受管理 HSM 的安全性網域資料，以在另一個 HSM 上進行匯出。</span><span class="sxs-lookup"><span data-stu-id="b5f96-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="b5f96-109">例子</span><span class="sxs-lookup"><span data-stu-id="b5f96-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f96-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5f96-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="b5f96-111">此命令會取取名為 testm分m 的受管理 HSM，並會將該受管理 HSM 安全網域的備份存到指定的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="b5f96-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="b5f96-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5f96-112">PARAMETERS</span></span>

### <span data-ttu-id="b5f96-113">-憑證</span><span class="sxs-lookup"><span data-stu-id="b5f96-113">-Certificates</span></span>
<span data-ttu-id="b5f96-114">用於加密安全性網域資料之憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="b5f96-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f96-115">-DefaultProfile</span></span>
<span data-ttu-id="b5f96-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5f96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f96-117">-強制</span><span class="sxs-lookup"><span data-stu-id="b5f96-117">-Force</span></span>
<span data-ttu-id="b5f96-118">指定是否要覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="b5f96-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="b5f96-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f96-119">-InputObject</span></span>
<span data-ttu-id="b5f96-120">代表受管理的 HSM 的物件。</span><span class="sxs-lookup"><span data-stu-id="b5f96-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="b5f96-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5f96-121">-Name</span></span>
<span data-ttu-id="b5f96-122">受管理 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5f96-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="b5f96-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b5f96-123">-OutputPath</span></span>
<span data-ttu-id="b5f96-124">指定要下載安全性網域資料的路徑。</span><span class="sxs-lookup"><span data-stu-id="b5f96-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f96-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5f96-125">-PassThru</span></span>
<span data-ttu-id="b5f96-126">指定時，當 Cmdlet 成功時，會返回布林值。</span><span class="sxs-lookup"><span data-stu-id="b5f96-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="b5f96-127">-下拉式</span><span class="sxs-lookup"><span data-stu-id="b5f96-127">-Quorum</span></span>
<span data-ttu-id="b5f96-128">解密安全性網域以復原所需的最低共用數目。</span><span class="sxs-lookup"><span data-stu-id="b5f96-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f96-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b5f96-129">-Confirm</span></span>
<span data-ttu-id="b5f96-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5f96-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f96-131">-WhatIf</span></span>
<span data-ttu-id="b5f96-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5f96-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5f96-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5f96-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f96-134">CommonParameters</span></span>
<span data-ttu-id="b5f96-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5f96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f96-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5f96-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f96-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b5f96-137">INPUTS</span></span>

### <span data-ttu-id="b5f96-138">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b5f96-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="b5f96-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b5f96-139">OUTPUTS</span></span>

### <span data-ttu-id="b5f96-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5f96-140">System.Boolean</span></span>

## <span data-ttu-id="b5f96-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b5f96-141">NOTES</span></span>

## <span data-ttu-id="b5f96-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5f96-142">RELATED LINKS</span></span>
