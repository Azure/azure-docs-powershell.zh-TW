---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138803"
---
# <span data-ttu-id="66a4d-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="66a4d-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="66a4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="66a4d-103">[資源] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="66a4d-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="66a4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="66a4d-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="66a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="66a4d-106">[資源] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="66a4d-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="66a4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="66a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="66a4d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66a4d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="66a4d-109">[專用主機] 的 [清單] configurationAssignments。</span><span class="sxs-lookup"><span data-stu-id="66a4d-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="66a4d-110">參數</span><span class="sxs-lookup"><span data-stu-id="66a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="66a4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a4d-111">-DefaultProfile</span></span>
<span data-ttu-id="66a4d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66a4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a4d-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="66a4d-113">-ProviderName</span></span>
<span data-ttu-id="66a4d-114">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="66a4d-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="66a4d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a4d-115">-ResourceGroupName</span></span>
<span data-ttu-id="66a4d-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66a4d-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="66a4d-117">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="66a4d-117">-ResourceName</span></span>
<span data-ttu-id="66a4d-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="66a4d-118">The resource name.</span></span>

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

### <span data-ttu-id="66a4d-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="66a4d-119">-ResourceParentName</span></span>
<span data-ttu-id="66a4d-120">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="66a4d-120">The parent resource name.</span></span>

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

### <span data-ttu-id="66a4d-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="66a4d-121">-ResourceParentType</span></span>
<span data-ttu-id="66a4d-122">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="66a4d-122">The parent resource type.</span></span>

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

### <span data-ttu-id="66a4d-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="66a4d-123">-ResourceType</span></span>
<span data-ttu-id="66a4d-124">資源類型。</span><span class="sxs-lookup"><span data-stu-id="66a4d-124">The resource type.</span></span>

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

### <span data-ttu-id="66a4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a4d-125">CommonParameters</span></span>
<span data-ttu-id="66a4d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66a4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a4d-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66a4d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a4d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="66a4d-128">INPUTS</span></span>

### <span data-ttu-id="66a4d-129">System.object</span><span class="sxs-lookup"><span data-stu-id="66a4d-129">System.String</span></span>

## <span data-ttu-id="66a4d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="66a4d-130">OUTPUTS</span></span>

### <span data-ttu-id="66a4d-131">PSConfigurationAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66a4d-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="66a4d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="66a4d-132">NOTES</span></span>

## <span data-ttu-id="66a4d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="66a4d-133">RELATED LINKS</span></span>
