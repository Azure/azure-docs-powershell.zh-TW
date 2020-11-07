---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793997"
---
# <span data-ttu-id="a63e1-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a63e1-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a63e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a63e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a63e1-103">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="a63e1-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="a63e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a63e1-104">SYNTAX</span></span>

### <span data-ttu-id="a63e1-105">關機 (預設) </span><span class="sxs-lookup"><span data-stu-id="a63e1-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63e1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a63e1-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a63e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="a63e1-107">DESCRIPTION</span></span>
<span data-ttu-id="a63e1-108">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="a63e1-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="a63e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="a63e1-109">EXAMPLES</span></span>

### <span data-ttu-id="a63e1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a63e1-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="a63e1-111">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="a63e1-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="a63e1-112">參數</span><span class="sxs-lookup"><span data-stu-id="a63e1-112">PARAMETERS</span></span>

### <span data-ttu-id="a63e1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a63e1-113">-Name</span></span>
<span data-ttu-id="a63e1-114">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a63e1-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="a63e1-115">-Location</span></span>
<span data-ttu-id="a63e1-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a63e1-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="a63e1-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a63e1-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a63e1-119">-ResourceId</span></span>
<span data-ttu-id="a63e1-120">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a63e1-120">Infrastructure role instance resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a63e1-121">-AsJob</span></span>
<span data-ttu-id="a63e1-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="a63e1-122">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a63e1-123">-Force</span></span>
<span data-ttu-id="a63e1-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a63e1-124">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63e1-125">-WhatIf</span></span>
<span data-ttu-id="a63e1-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a63e1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63e1-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a63e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63e1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a63e1-128">-Confirm</span></span>
<span data-ttu-id="a63e1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a63e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63e1-130">CommonParameters</span></span>
<span data-ttu-id="a63e1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a63e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63e1-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a63e1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63e1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a63e1-133">INPUTS</span></span>

## <span data-ttu-id="a63e1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a63e1-134">OUTPUTS</span></span>

## <span data-ttu-id="a63e1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a63e1-135">NOTES</span></span>

## <span data-ttu-id="a63e1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a63e1-136">RELATED LINKS</span></span>
