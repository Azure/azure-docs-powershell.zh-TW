---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968286"
---
# <span data-ttu-id="7c1c2-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7c1c2-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="7c1c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1c2-103">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="7c1c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c1c2-104">SYNTAX</span></span>

### <span data-ttu-id="7c1c2-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="7c1c2-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c1c2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c1c2-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c1c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="7c1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="7c1c2-108">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="7c1c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="7c1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="7c1c2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7c1c2-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="7c1c2-111">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="7c1c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="7c1c2-112">PARAMETERS</span></span>

### <span data-ttu-id="7c1c2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c1c2-113">-Name</span></span>
<span data-ttu-id="7c1c2-114">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-114">Name of the infrastructure role instance.</span></span>

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

### <span data-ttu-id="7c1c2-115">-位置</span><span class="sxs-lookup"><span data-stu-id="7c1c2-115">-Location</span></span>
<span data-ttu-id="7c1c2-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-116">Location of the resource.</span></span>

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

### <span data-ttu-id="7c1c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c1c2-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7c1c2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c1c2-119">-ResourceId</span></span>
<span data-ttu-id="7c1c2-120">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="7c1c2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c1c2-121">-AsJob</span></span>
<span data-ttu-id="7c1c2-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7c1c2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7c1c2-123">-Force</span></span>
<span data-ttu-id="7c1c2-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7c1c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1c2-125">-WhatIf</span></span>
<span data-ttu-id="7c1c2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1c2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1c2-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7c1c2-128">-Confirm</span></span>
<span data-ttu-id="7c1c2-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1c2-130">CommonParameters</span></span>
<span data-ttu-id="7c1c2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1c2-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c1c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1c2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7c1c2-133">INPUTS</span></span>

## <span data-ttu-id="7c1c2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7c1c2-134">OUTPUTS</span></span>

## <span data-ttu-id="7c1c2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7c1c2-135">NOTES</span></span>

## <span data-ttu-id="7c1c2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c1c2-136">RELATED LINKS</span></span>
