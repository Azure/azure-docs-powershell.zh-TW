---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443520"
---
# <span data-ttu-id="ddd7f-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ddd7f-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="ddd7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd7f-103">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="ddd7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddd7f-104">SYNTAX</span></span>

### <span data-ttu-id="ddd7f-105">關閉 (預設) </span><span class="sxs-lookup"><span data-stu-id="ddd7f-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd7f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd7f-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddd7f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ddd7f-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd7f-108">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="ddd7f-109">示例</span><span class="sxs-lookup"><span data-stu-id="ddd7f-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd7f-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ddd7f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="ddd7f-111">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="ddd7f-112">失敗時，會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="ddd7f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddd7f-113">PARAMETERS</span></span>

### <span data-ttu-id="ddd7f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd7f-114">-AsJob</span></span>
<span data-ttu-id="ddd7f-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ddd7f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd7f-116">-Force</span></span>
<span data-ttu-id="ddd7f-117">不要求確認</span><span class="sxs-lookup"><span data-stu-id="ddd7f-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="ddd7f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="ddd7f-118">-Location</span></span>
<span data-ttu-id="ddd7f-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd7f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddd7f-120">-Name</span></span>
<span data-ttu-id="ddd7f-121">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-121">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddd7f-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd7f-124">-ResourceId</span></span>
<span data-ttu-id="ddd7f-125">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="ddd7f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ddd7f-126">-Confirm</span></span>
<span data-ttu-id="ddd7f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd7f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd7f-128">-WhatIf</span></span>
<span data-ttu-id="ddd7f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd7f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd7f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd7f-131">CommonParameters</span></span>
<span data-ttu-id="ddd7f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd7f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddd7f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd7f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ddd7f-134">INPUTS</span></span>

## <span data-ttu-id="ddd7f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ddd7f-135">OUTPUTS</span></span>

## <span data-ttu-id="ddd7f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ddd7f-136">NOTES</span></span>

## <span data-ttu-id="ddd7f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddd7f-137">RELATED LINKS</span></span>

