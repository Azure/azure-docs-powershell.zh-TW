---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443052"
---
# <span data-ttu-id="0bcde-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0bcde-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0bcde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bcde-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcde-103">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="0bcde-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="0bcde-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bcde-104">SYNTAX</span></span>

### <span data-ttu-id="0bcde-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="0bcde-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bcde-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bcde-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bcde-107">說明</span><span class="sxs-lookup"><span data-stu-id="0bcde-107">DESCRIPTION</span></span>
<span data-ttu-id="0bcde-108">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="0bcde-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="0bcde-109">示例</span><span class="sxs-lookup"><span data-stu-id="0bcde-109">EXAMPLES</span></span>

### <span data-ttu-id="0bcde-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0bcde-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0bcde-111">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="0bcde-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="0bcde-112">參數</span><span class="sxs-lookup"><span data-stu-id="0bcde-112">PARAMETERS</span></span>

### <span data-ttu-id="0bcde-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bcde-113">-AsJob</span></span>
<span data-ttu-id="0bcde-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="0bcde-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0bcde-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0bcde-115">-Force</span></span>
<span data-ttu-id="0bcde-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0bcde-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0bcde-117">-位置</span><span class="sxs-lookup"><span data-stu-id="0bcde-117">-Location</span></span>
<span data-ttu-id="0bcde-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0bcde-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bcde-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bcde-119">-Name</span></span>
<span data-ttu-id="0bcde-120">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bcde-120">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bcde-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bcde-121">-ResourceGroupName</span></span>
<span data-ttu-id="0bcde-122">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0bcde-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bcde-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bcde-123">-ResourceId</span></span>
<span data-ttu-id="0bcde-124">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0bcde-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="0bcde-125">-確認</span><span class="sxs-lookup"><span data-stu-id="0bcde-125">-Confirm</span></span>
<span data-ttu-id="0bcde-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0bcde-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bcde-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bcde-127">-WhatIf</span></span>
<span data-ttu-id="0bcde-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0bcde-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bcde-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bcde-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bcde-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcde-130">CommonParameters</span></span>
<span data-ttu-id="0bcde-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bcde-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcde-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bcde-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcde-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0bcde-133">INPUTS</span></span>

## <span data-ttu-id="0bcde-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0bcde-134">OUTPUTS</span></span>

## <span data-ttu-id="0bcde-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0bcde-135">NOTES</span></span>

## <span data-ttu-id="0bcde-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bcde-136">RELATED LINKS</span></span>

