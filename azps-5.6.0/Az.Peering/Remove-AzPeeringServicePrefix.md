---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 3922492f4d72886e0608108811906387e31472b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911422"
---
# <span data-ttu-id="a9a37-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a9a37-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="a9a37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9a37-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a37-103">移除新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="a9a37-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="a9a37-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9a37-104">SYNTAX</span></span>

### <span data-ttu-id="a9a37-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a9a37-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a37-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9a37-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a37-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9a37-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a37-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9a37-108">DESCRIPTION</span></span>
<span data-ttu-id="a9a37-109">從對等服務移除對等服務首碼。</span><span class="sxs-lookup"><span data-stu-id="a9a37-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="a9a37-110">例子</span><span class="sxs-lookup"><span data-stu-id="a9a37-110">EXAMPLES</span></span>

### <span data-ttu-id="a9a37-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9a37-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="a9a37-112">移除對等服務物件的首碼</span><span class="sxs-lookup"><span data-stu-id="a9a37-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="a9a37-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a9a37-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="a9a37-114">移除對等服務資源識別碼的首碼。</span><span class="sxs-lookup"><span data-stu-id="a9a37-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="a9a37-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="a9a37-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="a9a37-116">移除對等服務資源組名和名稱的首碼</span><span class="sxs-lookup"><span data-stu-id="a9a37-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="a9a37-117">參數</span><span class="sxs-lookup"><span data-stu-id="a9a37-117">PARAMETERS</span></span>

### <span data-ttu-id="a9a37-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9a37-118">-AsJob</span></span>
<span data-ttu-id="a9a37-119">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="a9a37-119">Run in the background.</span></span>

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

### <span data-ttu-id="a9a37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a37-120">-DefaultProfile</span></span>
<span data-ttu-id="a9a37-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9a37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9a37-122">-強制</span><span class="sxs-lookup"><span data-stu-id="a9a37-122">-Force</span></span>
<span data-ttu-id="a9a37-123">強制完成作業</span><span class="sxs-lookup"><span data-stu-id="a9a37-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="a9a37-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9a37-124">-InputObject</span></span>
<span data-ttu-id="a9a37-125">使用Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a9a37-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a37-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9a37-126">-Name</span></span>
<span data-ttu-id="a9a37-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a37-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a37-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9a37-128">-PassThru</span></span>
<span data-ttu-id="a9a37-129">成功時，會以 True 為根據，或為失敗時為 False。</span><span class="sxs-lookup"><span data-stu-id="a9a37-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="a9a37-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="a9a37-130">-PrefixName</span></span>
<span data-ttu-id="a9a37-131">首碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a37-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a37-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a37-132">-ResourceGroupName</span></span>
<span data-ttu-id="a9a37-133">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9a37-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a37-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9a37-134">-ResourceId</span></span>
<span data-ttu-id="a9a37-135">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a37-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a37-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a9a37-136">-Confirm</span></span>
<span data-ttu-id="a9a37-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9a37-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a37-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a37-138">-WhatIf</span></span>
<span data-ttu-id="a9a37-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9a37-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a37-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9a37-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a37-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a37-141">CommonParameters</span></span>
<span data-ttu-id="a9a37-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9a37-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a37-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9a37-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a37-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a9a37-144">INPUTS</span></span>

### <span data-ttu-id="a9a37-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a9a37-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="a9a37-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a37-146">System.String</span></span>

## <span data-ttu-id="a9a37-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a9a37-147">OUTPUTS</span></span>

### <span data-ttu-id="a9a37-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9a37-148">System.Boolean</span></span>

## <span data-ttu-id="a9a37-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a9a37-149">NOTES</span></span>

## <span data-ttu-id="a9a37-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9a37-150">RELATED LINKS</span></span>
