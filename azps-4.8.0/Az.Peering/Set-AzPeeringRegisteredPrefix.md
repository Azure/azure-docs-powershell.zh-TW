---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128874"
---
# <span data-ttu-id="1fa3f-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="1fa3f-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="1fa3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fa3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa3f-103">從上層對等資源設定或更新已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="1fa3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fa3f-104">SYNTAX</span></span>

### <span data-ttu-id="1fa3f-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="1fa3f-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fa3f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1fa3f-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fa3f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa3f-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fa3f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1fa3f-108">DESCRIPTION</span></span>
<span data-ttu-id="1fa3f-109">允許從父對等資源更新已註冊的前置詞。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="1fa3f-110">示例</span><span class="sxs-lookup"><span data-stu-id="1fa3f-110">EXAMPLES</span></span>

### <span data-ttu-id="1fa3f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1fa3f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="1fa3f-112">依資源識別碼更新前置詞。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="1fa3f-113">參數</span><span class="sxs-lookup"><span data-stu-id="1fa3f-113">PARAMETERS</span></span>

### <span data-ttu-id="1fa3f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fa3f-114">-AsJob</span></span>
<span data-ttu-id="1fa3f-115">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-115">Run in the background.</span></span>

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

### <span data-ttu-id="1fa3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa3f-116">-DefaultProfile</span></span>
<span data-ttu-id="1fa3f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fa3f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fa3f-118">-InputObject</span></span>
<span data-ttu-id="1fa3f-119">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="1fa3f-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa3f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fa3f-120">-Name</span></span>
<span data-ttu-id="1fa3f-121">前置詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa3f-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="1fa3f-122">-PeeringName</span></span>
<span data-ttu-id="1fa3f-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa3f-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1fa3f-124">-Prefix</span></span>
<span data-ttu-id="1fa3f-125">會話 IPv4 首碼</span><span class="sxs-lookup"><span data-stu-id="1fa3f-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="1fa3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fa3f-127">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa3f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa3f-128">-ResourceId</span></span>
<span data-ttu-id="1fa3f-129">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-129">The resource id string name.</span></span>

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

### <span data-ttu-id="1fa3f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1fa3f-130">-Confirm</span></span>
<span data-ttu-id="1fa3f-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa3f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa3f-132">-WhatIf</span></span>
<span data-ttu-id="1fa3f-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fa3f-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa3f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa3f-135">CommonParameters</span></span>
<span data-ttu-id="1fa3f-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa3f-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fa3f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa3f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1fa3f-138">INPUTS</span></span>

### <span data-ttu-id="1fa3f-139">PSPeeringRegisteredPrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="1fa3f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="1fa3f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1fa3f-140">System.String</span></span>

## <span data-ttu-id="1fa3f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1fa3f-141">OUTPUTS</span></span>

### <span data-ttu-id="1fa3f-142">PSPeeringRegisteredPrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="1fa3f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="1fa3f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1fa3f-143">NOTES</span></span>

## <span data-ttu-id="1fa3f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fa3f-144">RELATED LINKS</span></span>