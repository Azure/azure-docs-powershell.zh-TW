---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968126"
---
# <span data-ttu-id="11d25-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="11d25-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="11d25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11d25-102">SYNOPSIS</span></span>
<span data-ttu-id="11d25-103">重新開機基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="11d25-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="11d25-104">句法</span><span class="sxs-lookup"><span data-stu-id="11d25-104">SYNTAX</span></span>

### <span data-ttu-id="11d25-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="11d25-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d25-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d25-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11d25-107">說明</span><span class="sxs-lookup"><span data-stu-id="11d25-107">DESCRIPTION</span></span>
<span data-ttu-id="11d25-108">重新開機基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="11d25-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="11d25-109">示例</span><span class="sxs-lookup"><span data-stu-id="11d25-109">EXAMPLES</span></span>

### <span data-ttu-id="11d25-110">範例1</span><span class="sxs-lookup"><span data-stu-id="11d25-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="11d25-111">重新開機基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="11d25-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="11d25-112">參數</span><span class="sxs-lookup"><span data-stu-id="11d25-112">PARAMETERS</span></span>

### <span data-ttu-id="11d25-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="11d25-113">-Name</span></span>
<span data-ttu-id="11d25-114">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="11d25-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d25-115">-位置</span><span class="sxs-lookup"><span data-stu-id="11d25-115">-Location</span></span>
<span data-ttu-id="11d25-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="11d25-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d25-117">-ResourceGroupName</span></span>
<span data-ttu-id="11d25-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="11d25-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d25-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d25-119">-ResourceId</span></span>
<span data-ttu-id="11d25-120">基礎結構角色實例資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11d25-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="11d25-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11d25-121">-AsJob</span></span>
<span data-ttu-id="11d25-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="11d25-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="11d25-123">-Force</span><span class="sxs-lookup"><span data-stu-id="11d25-123">-Force</span></span>
<span data-ttu-id="11d25-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="11d25-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="11d25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d25-125">-WhatIf</span></span>
<span data-ttu-id="11d25-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11d25-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d25-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11d25-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d25-128">-確認</span><span class="sxs-lookup"><span data-stu-id="11d25-128">-Confirm</span></span>
<span data-ttu-id="11d25-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11d25-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d25-130">CommonParameters</span></span>
<span data-ttu-id="11d25-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11d25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d25-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11d25-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d25-133">輸入</span><span class="sxs-lookup"><span data-stu-id="11d25-133">INPUTS</span></span>

## <span data-ttu-id="11d25-134">輸出</span><span class="sxs-lookup"><span data-stu-id="11d25-134">OUTPUTS</span></span>

## <span data-ttu-id="11d25-135">筆記</span><span class="sxs-lookup"><span data-stu-id="11d25-135">NOTES</span></span>

## <span data-ttu-id="11d25-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="11d25-136">RELATED LINKS</span></span>
