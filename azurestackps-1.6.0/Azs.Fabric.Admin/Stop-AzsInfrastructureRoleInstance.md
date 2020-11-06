---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623206"
---
# <span data-ttu-id="df580-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="df580-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="df580-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df580-102">SYNOPSIS</span></span>
<span data-ttu-id="df580-103">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="df580-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="df580-104">句法</span><span class="sxs-lookup"><span data-stu-id="df580-104">SYNTAX</span></span>

### <span data-ttu-id="df580-105">關機 (預設) </span><span class="sxs-lookup"><span data-stu-id="df580-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df580-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="df580-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df580-107">說明</span><span class="sxs-lookup"><span data-stu-id="df580-107">DESCRIPTION</span></span>
<span data-ttu-id="df580-108">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="df580-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="df580-109">示例</span><span class="sxs-lookup"><span data-stu-id="df580-109">EXAMPLES</span></span>

### <span data-ttu-id="df580-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df580-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="df580-111">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="df580-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="df580-112">參數</span><span class="sxs-lookup"><span data-stu-id="df580-112">PARAMETERS</span></span>

### <span data-ttu-id="df580-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df580-113">-AsJob</span></span>
<span data-ttu-id="df580-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="df580-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="df580-115">-Force</span><span class="sxs-lookup"><span data-stu-id="df580-115">-Force</span></span>
<span data-ttu-id="df580-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="df580-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="df580-117">-位置</span><span class="sxs-lookup"><span data-stu-id="df580-117">-Location</span></span>
<span data-ttu-id="df580-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="df580-118">Location of the resource.</span></span>

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

### <span data-ttu-id="df580-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="df580-119">-Name</span></span>
<span data-ttu-id="df580-120">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="df580-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="df580-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df580-121">-ResourceGroupName</span></span>
<span data-ttu-id="df580-122">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="df580-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="df580-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df580-123">-ResourceId</span></span>
<span data-ttu-id="df580-124">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="df580-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="df580-125">-確認</span><span class="sxs-lookup"><span data-stu-id="df580-125">-Confirm</span></span>
<span data-ttu-id="df580-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df580-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df580-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df580-127">-WhatIf</span></span>
<span data-ttu-id="df580-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df580-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df580-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df580-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df580-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df580-130">CommonParameters</span></span>
<span data-ttu-id="df580-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df580-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df580-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df580-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df580-133">輸入</span><span class="sxs-lookup"><span data-stu-id="df580-133">INPUTS</span></span>

## <span data-ttu-id="df580-134">輸出</span><span class="sxs-lookup"><span data-stu-id="df580-134">OUTPUTS</span></span>

## <span data-ttu-id="df580-135">筆記</span><span class="sxs-lookup"><span data-stu-id="df580-135">NOTES</span></span>

## <span data-ttu-id="df580-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="df580-136">RELATED LINKS</span></span>
