---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 3175685478afada44e8870e772a56ce91992bbc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914805"
---
# <span data-ttu-id="204df-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="204df-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="204df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="204df-102">SYNOPSIS</span></span>
<span data-ttu-id="204df-103">將先前匯出的安全網域資料匯至受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="204df-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="204df-104">語法</span><span class="sxs-lookup"><span data-stu-id="204df-104">SYNTAX</span></span>

### <span data-ttu-id="204df-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="204df-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="204df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="204df-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="204df-107">描述</span><span class="sxs-lookup"><span data-stu-id="204df-107">DESCRIPTION</span></span>
<span data-ttu-id="204df-108">此 Cmdlet 會匯出先前匯出的安全網域資料至受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="204df-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="204df-109">例子</span><span class="sxs-lookup"><span data-stu-id="204df-109">EXAMPLES</span></span>

### <span data-ttu-id="204df-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="204df-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="204df-111">首先，需要提供金鑰以解密安全性網域資料。</span><span class="sxs-lookup"><span data-stu-id="204df-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="204df-112">然後 **，Import-AzKeyVaultSecurityDomain** 命令會使用這些金鑰，將先前備份的安全網域資料還原到受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="204df-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="204df-113">參數</span><span class="sxs-lookup"><span data-stu-id="204df-113">PARAMETERS</span></span>

### <span data-ttu-id="204df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204df-114">-DefaultProfile</span></span>
<span data-ttu-id="204df-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="204df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204df-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="204df-116">-InputObject</span></span>
<span data-ttu-id="204df-117">代表受管理的 HSM 的物件。</span><span class="sxs-lookup"><span data-stu-id="204df-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="204df-118">-按鍵</span><span class="sxs-lookup"><span data-stu-id="204df-118">-Keys</span></span>
<span data-ttu-id="204df-119">用於解密安全性網域資料之金鑰的資訊。</span><span class="sxs-lookup"><span data-stu-id="204df-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="204df-120">請參閱如何建構的範例。</span><span class="sxs-lookup"><span data-stu-id="204df-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="204df-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="204df-121">-Name</span></span>
<span data-ttu-id="204df-122">受管理 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="204df-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="204df-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="204df-123">-PassThru</span></span>
<span data-ttu-id="204df-124">指定時，當 Cmdlet 成功時，會返回布林值。</span><span class="sxs-lookup"><span data-stu-id="204df-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="204df-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="204df-125">-SecurityDomainPath</span></span>
<span data-ttu-id="204df-126">指定加密安全性網域資料的路徑。</span><span class="sxs-lookup"><span data-stu-id="204df-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="204df-127">-確認</span><span class="sxs-lookup"><span data-stu-id="204df-127">-Confirm</span></span>
<span data-ttu-id="204df-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="204df-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204df-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204df-129">-WhatIf</span></span>
<span data-ttu-id="204df-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="204df-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="204df-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="204df-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204df-132">CommonParameters</span></span>
<span data-ttu-id="204df-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="204df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204df-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="204df-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204df-135">輸入</span><span class="sxs-lookup"><span data-stu-id="204df-135">INPUTS</span></span>

### <span data-ttu-id="204df-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="204df-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="204df-137">輸出</span><span class="sxs-lookup"><span data-stu-id="204df-137">OUTPUTS</span></span>

### <span data-ttu-id="204df-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="204df-138">System.Boolean</span></span>

## <span data-ttu-id="204df-139">筆記</span><span class="sxs-lookup"><span data-stu-id="204df-139">NOTES</span></span>

## <span data-ttu-id="204df-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="204df-140">RELATED LINKS</span></span>
