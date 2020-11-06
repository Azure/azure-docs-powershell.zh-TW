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
ms.locfileid: "93443040"
---
# <span data-ttu-id="41cc1-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="41cc1-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="41cc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="41cc1-103">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="41cc1-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="41cc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="41cc1-104">SYNTAX</span></span>

### <span data-ttu-id="41cc1-105">關閉 (預設) </span><span class="sxs-lookup"><span data-stu-id="41cc1-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41cc1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41cc1-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41cc1-107">說明</span><span class="sxs-lookup"><span data-stu-id="41cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="41cc1-108">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="41cc1-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="41cc1-109">示例</span><span class="sxs-lookup"><span data-stu-id="41cc1-109">EXAMPLES</span></span>

### <span data-ttu-id="41cc1-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41cc1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="41cc1-111">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="41cc1-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="41cc1-112">失敗時，會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="41cc1-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="41cc1-113">參數</span><span class="sxs-lookup"><span data-stu-id="41cc1-113">PARAMETERS</span></span>

### <span data-ttu-id="41cc1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41cc1-114">-AsJob</span></span>
<span data-ttu-id="41cc1-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="41cc1-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41cc1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="41cc1-116">-Force</span></span>
<span data-ttu-id="41cc1-117">不要求確認</span><span class="sxs-lookup"><span data-stu-id="41cc1-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="41cc1-118">-位置</span><span class="sxs-lookup"><span data-stu-id="41cc1-118">-Location</span></span>
<span data-ttu-id="41cc1-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="41cc1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="41cc1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="41cc1-120">-Name</span></span>
<span data-ttu-id="41cc1-121">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cc1-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="41cc1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cc1-122">-ResourceGroupName</span></span>
<span data-ttu-id="41cc1-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="41cc1-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="41cc1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41cc1-124">-ResourceId</span></span>
<span data-ttu-id="41cc1-125">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="41cc1-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="41cc1-126">-確認</span><span class="sxs-lookup"><span data-stu-id="41cc1-126">-Confirm</span></span>
<span data-ttu-id="41cc1-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41cc1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cc1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cc1-128">-WhatIf</span></span>
<span data-ttu-id="41cc1-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41cc1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cc1-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41cc1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cc1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cc1-131">CommonParameters</span></span>
<span data-ttu-id="41cc1-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41cc1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cc1-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41cc1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cc1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="41cc1-134">INPUTS</span></span>

## <span data-ttu-id="41cc1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="41cc1-135">OUTPUTS</span></span>

## <span data-ttu-id="41cc1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="41cc1-136">NOTES</span></span>

## <span data-ttu-id="41cc1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="41cc1-137">RELATED LINKS</span></span>
