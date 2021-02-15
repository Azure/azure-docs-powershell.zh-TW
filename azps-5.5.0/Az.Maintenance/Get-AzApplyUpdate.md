---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142293"
---
# <span data-ttu-id="5c2a8-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="5c2a8-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="5c2a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2a8-103">追蹤資源的維護更新</span><span class="sxs-lookup"><span data-stu-id="5c2a8-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="5c2a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c2a8-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c2a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="5c2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="5c2a8-106">追蹤資源的維護更新</span><span class="sxs-lookup"><span data-stu-id="5c2a8-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="5c2a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="5c2a8-107">EXAMPLES</span></span>

### <span data-ttu-id="5c2a8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5c2a8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="5c2a8-109">追蹤資源的維護更新</span><span class="sxs-lookup"><span data-stu-id="5c2a8-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="5c2a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c2a8-110">PARAMETERS</span></span>

### <span data-ttu-id="5c2a8-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="5c2a8-111">-ApplyUpdateName</span></span>
<span data-ttu-id="5c2a8-112">[套用更新資源名稱]。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2a8-113">-DefaultProfile</span></span>
<span data-ttu-id="5c2a8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2a8-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="5c2a8-115">-ProviderName</span></span>
<span data-ttu-id="5c2a8-116">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c2a8-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-119">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="5c2a8-119">-ResourceName</span></span>
<span data-ttu-id="5c2a8-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="5c2a8-121">-ResourceParentName</span></span>
<span data-ttu-id="5c2a8-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="5c2a8-123">-ResourceParentType</span></span>
<span data-ttu-id="5c2a8-124">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5c2a8-125">-ResourceType</span></span>
<span data-ttu-id="5c2a8-126">資源類型。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2a8-127">CommonParameters</span></span>
<span data-ttu-id="5c2a8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2a8-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c2a8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2a8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5c2a8-130">INPUTS</span></span>

### <span data-ttu-id="5c2a8-131">System.object</span><span class="sxs-lookup"><span data-stu-id="5c2a8-131">System.String</span></span>

## <span data-ttu-id="5c2a8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5c2a8-132">OUTPUTS</span></span>

### <span data-ttu-id="5c2a8-133">PSApplyUpdate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5c2a8-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="5c2a8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5c2a8-134">NOTES</span></span>

## <span data-ttu-id="5c2a8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c2a8-135">RELATED LINKS</span></span>
