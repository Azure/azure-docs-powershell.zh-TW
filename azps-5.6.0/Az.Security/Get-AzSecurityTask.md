---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
ms.openlocfilehash: cd3973b76a78386db26154d765563432f6167875
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909465"
---
# <span data-ttu-id="c4386-101">Get-AzSecurityTask</span><span class="sxs-lookup"><span data-stu-id="c4386-101">Get-AzSecurityTask</span></span>

## <span data-ttu-id="c4386-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c4386-102">SYNOPSIS</span></span>
<span data-ttu-id="c4386-103">獲得 Azure 資訊安全中心建議您執行的安全性工作，以強化您的安全性狀態。</span><span class="sxs-lookup"><span data-stu-id="c4386-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

## <span data-ttu-id="c4386-104">語法</span><span class="sxs-lookup"><span data-stu-id="c4386-104">SYNTAX</span></span>

### <span data-ttu-id="c4386-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c4386-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4386-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="c4386-106">ResourceGroupScope</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4386-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c4386-107">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4386-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c4386-108">SubscriptionLevelResource</span></span>
```
Get-AzSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4386-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4386-109">ResourceId</span></span>
```
Get-AzSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4386-110">描述</span><span class="sxs-lookup"><span data-stu-id="c4386-110">DESCRIPTION</span></span>
<span data-ttu-id="c4386-111">Azure 資訊安全中心會掃描您的資源，以偵測潛在的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="c4386-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="c4386-112">此 Cmdlet 可讓您探索 Azure 資訊安全中心建議您執行的安全性工作。</span><span class="sxs-lookup"><span data-stu-id="c4386-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="c4386-113">例子</span><span class="sxs-lookup"><span data-stu-id="c4386-113">EXAMPLES</span></span>

### <span data-ttu-id="c4386-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="c4386-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="c4386-115">獲得在訂閱內資源上發現的所有安全性工作。</span><span class="sxs-lookup"><span data-stu-id="c4386-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="c4386-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="c4386-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="c4386-117">獲得在資源群組內資源上發現的所有安全性工作。</span><span class="sxs-lookup"><span data-stu-id="c4386-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="c4386-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="c4386-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="c4386-119">獲得特定的安全性工作。</span><span class="sxs-lookup"><span data-stu-id="c4386-119">Gets a specific security task.</span></span>

## <span data-ttu-id="c4386-120">參數</span><span class="sxs-lookup"><span data-stu-id="c4386-120">PARAMETERS</span></span>

### <span data-ttu-id="c4386-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4386-121">-DefaultProfile</span></span>
<span data-ttu-id="c4386-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4386-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4386-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4386-123">-Name</span></span>
<span data-ttu-id="c4386-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c4386-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4386-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4386-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4386-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c4386-126">Resource group name.</span></span>

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

### <span data-ttu-id="c4386-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4386-127">-ResourceId</span></span>
<span data-ttu-id="c4386-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4386-128">Resource ID.</span></span>

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

### <span data-ttu-id="c4386-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4386-129">CommonParameters</span></span>
<span data-ttu-id="c4386-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c4386-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4386-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4386-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4386-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c4386-132">INPUTS</span></span>

### <span data-ttu-id="c4386-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4386-133">System.String</span></span>

## <span data-ttu-id="c4386-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c4386-134">OUTPUTS</span></span>

### <span data-ttu-id="c4386-135">Microsoft.Azure.Commands.security.models.Tasks.PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="c4386-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="c4386-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c4386-136">NOTES</span></span>

## <span data-ttu-id="c4386-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4386-137">RELATED LINKS</span></span>
