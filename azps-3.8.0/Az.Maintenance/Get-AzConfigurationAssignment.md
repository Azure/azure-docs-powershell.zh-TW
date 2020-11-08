---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965671"
---
# <span data-ttu-id="c1dd9-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c1dd9-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="c1dd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1dd9-103">[資源] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="c1dd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1dd9-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1dd9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="c1dd9-106">[資源] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="c1dd9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c1dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="c1dd9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c1dd9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="c1dd9-109">[專用主機] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="c1dd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1dd9-110">PARAMETERS</span></span>

### <span data-ttu-id="c1dd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1dd9-111">-DefaultProfile</span></span>
<span data-ttu-id="c1dd9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1dd9-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c1dd9-113">-ProviderName</span></span>
<span data-ttu-id="c1dd9-114">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="c1dd9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1dd9-115">-ResourceGroupName</span></span>
<span data-ttu-id="c1dd9-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="c1dd9-117">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="c1dd9-117">-ResourceName</span></span>
<span data-ttu-id="c1dd9-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-118">The resource name.</span></span>

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

### <span data-ttu-id="c1dd9-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="c1dd9-119">-ResourceParentName</span></span>
<span data-ttu-id="c1dd9-120">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-120">The parent resource name.</span></span>

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

### <span data-ttu-id="c1dd9-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="c1dd9-121">-ResourceParentType</span></span>
<span data-ttu-id="c1dd9-122">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-122">The parent resource type.</span></span>

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

### <span data-ttu-id="c1dd9-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c1dd9-123">-ResourceType</span></span>
<span data-ttu-id="c1dd9-124">資源類型。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-124">The resource type.</span></span>

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

### <span data-ttu-id="c1dd9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1dd9-125">CommonParameters</span></span>
<span data-ttu-id="c1dd9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1dd9-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c1dd9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1dd9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c1dd9-128">INPUTS</span></span>

### <span data-ttu-id="c1dd9-129">System.object</span><span class="sxs-lookup"><span data-stu-id="c1dd9-129">System.String</span></span>

## <span data-ttu-id="c1dd9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c1dd9-130">OUTPUTS</span></span>

### <span data-ttu-id="c1dd9-131">PSConfigurationAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c1dd9-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="c1dd9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c1dd9-132">NOTES</span></span>

## <span data-ttu-id="c1dd9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1dd9-133">RELATED LINKS</span></span>