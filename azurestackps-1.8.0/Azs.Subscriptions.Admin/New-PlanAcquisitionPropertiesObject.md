---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793632"
---
# <span data-ttu-id="35f70-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="35f70-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="35f70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35f70-102">SYNOPSIS</span></span>
<span data-ttu-id="35f70-103">代表購買訂閱的附加元件方案。</span><span class="sxs-lookup"><span data-stu-id="35f70-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="35f70-104">句法</span><span class="sxs-lookup"><span data-stu-id="35f70-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="35f70-105">說明</span><span class="sxs-lookup"><span data-stu-id="35f70-105">DESCRIPTION</span></span>
<span data-ttu-id="35f70-106">代表購買訂閱的附加元件方案。</span><span class="sxs-lookup"><span data-stu-id="35f70-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="35f70-107">示例</span><span class="sxs-lookup"><span data-stu-id="35f70-107">EXAMPLES</span></span>

### <span data-ttu-id="35f70-108">範例1</span><span class="sxs-lookup"><span data-stu-id="35f70-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="35f70-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="35f70-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="35f70-110">參數</span><span class="sxs-lookup"><span data-stu-id="35f70-110">PARAMETERS</span></span>

### <span data-ttu-id="35f70-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="35f70-111">-AcquisitionId</span></span>
<span data-ttu-id="35f70-112">購置識別碼。</span><span class="sxs-lookup"><span data-stu-id="35f70-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="35f70-113">-AcquisitionTime</span></span>
<span data-ttu-id="35f70-114">購置時間。</span><span class="sxs-lookup"><span data-stu-id="35f70-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="35f70-115">-ExternalReferenceId</span></span>
<span data-ttu-id="35f70-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="35f70-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="35f70-117">-Id</span></span>
<span data-ttu-id="35f70-118">租使用者訂閱內容中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="35f70-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="35f70-119">-PlanId</span></span>
<span data-ttu-id="35f70-120">租使用者訂閱內容中的 [規劃識別碼]。</span><span class="sxs-lookup"><span data-stu-id="35f70-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="35f70-121">-ProvisioningState</span></span>
<span data-ttu-id="35f70-122">[提供] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="35f70-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f70-123">CommonParameters</span></span>
<span data-ttu-id="35f70-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35f70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f70-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35f70-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f70-126">輸入</span><span class="sxs-lookup"><span data-stu-id="35f70-126">INPUTS</span></span>

## <span data-ttu-id="35f70-127">輸出</span><span class="sxs-lookup"><span data-stu-id="35f70-127">OUTPUTS</span></span>

## <span data-ttu-id="35f70-128">筆記</span><span class="sxs-lookup"><span data-stu-id="35f70-128">NOTES</span></span>

## <span data-ttu-id="35f70-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="35f70-129">RELATED LINKS</span></span>

