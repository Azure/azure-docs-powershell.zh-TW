---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968326"
---
# <span data-ttu-id="59054-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="59054-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="59054-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59054-102">SYNOPSIS</span></span>
<span data-ttu-id="59054-103">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="59054-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="59054-104">句法</span><span class="sxs-lookup"><span data-stu-id="59054-104">SYNTAX</span></span>

### <span data-ttu-id="59054-105">關閉 (預設) </span><span class="sxs-lookup"><span data-stu-id="59054-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59054-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59054-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59054-107">說明</span><span class="sxs-lookup"><span data-stu-id="59054-107">DESCRIPTION</span></span>
<span data-ttu-id="59054-108">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="59054-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="59054-109">示例</span><span class="sxs-lookup"><span data-stu-id="59054-109">EXAMPLES</span></span>

### <span data-ttu-id="59054-110">範例1</span><span class="sxs-lookup"><span data-stu-id="59054-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="59054-111">關閉基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="59054-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="59054-112">失敗時，會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="59054-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="59054-113">參數</span><span class="sxs-lookup"><span data-stu-id="59054-113">PARAMETERS</span></span>

### <span data-ttu-id="59054-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="59054-114">-Name</span></span>
<span data-ttu-id="59054-115">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="59054-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="59054-116">-位置</span><span class="sxs-lookup"><span data-stu-id="59054-116">-Location</span></span>
<span data-ttu-id="59054-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="59054-117">Location of the resource.</span></span>

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

### <span data-ttu-id="59054-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59054-118">-ResourceGroupName</span></span>
<span data-ttu-id="59054-119">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="59054-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="59054-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59054-120">-ResourceId</span></span>
<span data-ttu-id="59054-121">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="59054-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="59054-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59054-122">-AsJob</span></span>
<span data-ttu-id="59054-123">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="59054-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="59054-124">-Force</span><span class="sxs-lookup"><span data-stu-id="59054-124">-Force</span></span>
<span data-ttu-id="59054-125">不要求確認</span><span class="sxs-lookup"><span data-stu-id="59054-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="59054-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59054-126">-WhatIf</span></span>
<span data-ttu-id="59054-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59054-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59054-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59054-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59054-129">-確認</span><span class="sxs-lookup"><span data-stu-id="59054-129">-Confirm</span></span>
<span data-ttu-id="59054-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59054-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59054-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59054-131">CommonParameters</span></span>
<span data-ttu-id="59054-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59054-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59054-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59054-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59054-134">輸入</span><span class="sxs-lookup"><span data-stu-id="59054-134">INPUTS</span></span>

## <span data-ttu-id="59054-135">輸出</span><span class="sxs-lookup"><span data-stu-id="59054-135">OUTPUTS</span></span>

## <span data-ttu-id="59054-136">筆記</span><span class="sxs-lookup"><span data-stu-id="59054-136">NOTES</span></span>

## <span data-ttu-id="59054-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="59054-137">RELATED LINKS</span></span>
