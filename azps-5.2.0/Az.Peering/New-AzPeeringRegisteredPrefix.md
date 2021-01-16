---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279758"
---
# <span data-ttu-id="1d129-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="1d129-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="1d129-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d129-102">SYNOPSIS</span></span>
<span data-ttu-id="1d129-103">針對對等物件建立已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="1d129-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="1d129-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d129-104">SYNTAX</span></span>

### <span data-ttu-id="1d129-105">ByResourceGroupAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="1d129-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d129-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1d129-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d129-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d129-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d129-108">說明</span><span class="sxs-lookup"><span data-stu-id="1d129-108">DESCRIPTION</span></span>
<span data-ttu-id="1d129-109">針對對等物件建立已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="1d129-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="1d129-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d129-110">EXAMPLES</span></span>

### <span data-ttu-id="1d129-111">取得對等與建立已註冊的首碼</span><span class="sxs-lookup"><span data-stu-id="1d129-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="1d129-112">取得您想要新增已註冊的首碼的對等。</span><span class="sxs-lookup"><span data-stu-id="1d129-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="1d129-113">然後將它傳遞到 commandlet。</span><span class="sxs-lookup"><span data-stu-id="1d129-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="1d129-114">使用對等 resourceId 建立已註冊的 asn</span><span class="sxs-lookup"><span data-stu-id="1d129-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="1d129-115">參數</span><span class="sxs-lookup"><span data-stu-id="1d129-115">PARAMETERS</span></span>

### <span data-ttu-id="1d129-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d129-116">-AsJob</span></span>
<span data-ttu-id="1d129-117">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="1d129-117">Run in the background.</span></span>

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

### <span data-ttu-id="1d129-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d129-118">-DefaultProfile</span></span>
<span data-ttu-id="1d129-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d129-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d129-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d129-120">-InputObject</span></span>
<span data-ttu-id="1d129-121">使用 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="1d129-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d129-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d129-122">-Name</span></span>
<span data-ttu-id="1d129-123">前置詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d129-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d129-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="1d129-124">-PeeringName</span></span>
<span data-ttu-id="1d129-125">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="1d129-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1d129-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1d129-126">-Prefix</span></span>
<span data-ttu-id="1d129-127">會話 IPv4 首碼</span><span class="sxs-lookup"><span data-stu-id="1d129-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="1d129-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d129-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d129-129">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1d129-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1d129-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d129-130">-ResourceId</span></span>
<span data-ttu-id="1d129-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="1d129-131">The resource id string name.</span></span>

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

### <span data-ttu-id="1d129-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1d129-132">-Confirm</span></span>
<span data-ttu-id="1d129-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d129-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d129-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d129-134">-WhatIf</span></span>
<span data-ttu-id="1d129-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d129-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d129-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d129-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d129-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d129-137">CommonParameters</span></span>
<span data-ttu-id="1d129-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d129-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d129-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d129-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d129-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1d129-140">INPUTS</span></span>

### <span data-ttu-id="1d129-141">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="1d129-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="1d129-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1d129-142">System.String</span></span>

## <span data-ttu-id="1d129-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1d129-143">OUTPUTS</span></span>

### <span data-ttu-id="1d129-144">PSPeeringRegisteredPrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="1d129-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="1d129-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1d129-145">NOTES</span></span>

## <span data-ttu-id="1d129-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d129-146">RELATED LINKS</span></span>
