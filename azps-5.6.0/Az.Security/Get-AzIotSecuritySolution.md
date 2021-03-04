---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: d0bcbaf0edee0a0631621c0dccc73f8d6eda4c74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907301"
---
# <span data-ttu-id="75fb4-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="75fb4-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="75fb4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="75fb4-103">取得 IoT 安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="75fb4-103">Get IoT security solution</span></span>

## <span data-ttu-id="75fb4-104">語法</span><span class="sxs-lookup"><span data-stu-id="75fb4-104">SYNTAX</span></span>

### <span data-ttu-id="75fb4-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="75fb4-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75fb4-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="75fb4-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb4-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="75fb4-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75fb4-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75fb4-109">描述</span><span class="sxs-lookup"><span data-stu-id="75fb4-109">DESCRIPTION</span></span>
<span data-ttu-id="75fb4-110">Cmdlet Get-AzIotSecuritySolution會返回一或多個 iot 安全性解決方案。</span><span class="sxs-lookup"><span data-stu-id="75fb4-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="75fb4-111">IoT 安全性解決方案會收集 iot 裝置和 iot 中樞的安全性資料和事件，協助防範和偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="75fb4-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="75fb4-112">例子</span><span class="sxs-lookup"><span data-stu-id="75fb4-112">EXAMPLES</span></span>

### <span data-ttu-id="75fb4-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="75fb4-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="75fb4-114">在資源群組 「MyResourceGroup」 中取得「MySample」解決方案</span><span class="sxs-lookup"><span data-stu-id="75fb4-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="75fb4-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="75fb4-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="75fb4-116">取得資源群組 "MyResourceGroup" 中所有安全性解決方案的清單</span><span class="sxs-lookup"><span data-stu-id="75fb4-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="75fb4-117">參數</span><span class="sxs-lookup"><span data-stu-id="75fb4-117">PARAMETERS</span></span>

### <span data-ttu-id="75fb4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fb4-118">-DefaultProfile</span></span>
<span data-ttu-id="75fb4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75fb4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75fb4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="75fb4-120">-Name</span></span>
<span data-ttu-id="75fb4-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="75fb4-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75fb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75fb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="75fb4-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="75fb4-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75fb4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75fb4-124">-ResourceId</span></span>
<span data-ttu-id="75fb4-125">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="75fb4-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75fb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fb4-126">CommonParameters</span></span>
<span data-ttu-id="75fb4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75fb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fb4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75fb4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fb4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="75fb4-129">INPUTS</span></span>

### <span data-ttu-id="75fb4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="75fb4-130">System.String</span></span>

## <span data-ttu-id="75fb4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="75fb4-131">OUTPUTS</span></span>

### <span data-ttu-id="75fb4-132">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="75fb4-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="75fb4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="75fb4-133">NOTES</span></span>

## <span data-ttu-id="75fb4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="75fb4-134">RELATED LINKS</span></span>
