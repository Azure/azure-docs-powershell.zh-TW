---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: cb077b2bdc6c91ccb3dc1c9099490c1d8bf6bea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917097"
---
# <span data-ttu-id="23207-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="23207-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="23207-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23207-102">SYNOPSIS</span></span>
<span data-ttu-id="23207-103">獲得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="23207-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="23207-104">語法</span><span class="sxs-lookup"><span data-stu-id="23207-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="23207-105">描述</span><span class="sxs-lookup"><span data-stu-id="23207-105">DESCRIPTION</span></span>
<span data-ttu-id="23207-106">獲得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="23207-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="23207-107">例子</span><span class="sxs-lookup"><span data-stu-id="23207-107">EXAMPLES</span></span>

### <span data-ttu-id="23207-108">範例 1：取得雲端服務實例視圖</span><span class="sxs-lookup"><span data-stu-id="23207-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="23207-109">此 Cmdlet 會獲得名為 ContosoCS 的雲端服務實例視圖，該服務屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="23207-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="23207-110">參數</span><span class="sxs-lookup"><span data-stu-id="23207-110">PARAMETERS</span></span>

### <span data-ttu-id="23207-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="23207-111">-CloudServiceName</span></span>
<span data-ttu-id="23207-112">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="23207-112">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23207-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23207-113">-DefaultProfile</span></span>
<span data-ttu-id="23207-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23207-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23207-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23207-115">-ResourceGroupName</span></span>
<span data-ttu-id="23207-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23207-116">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23207-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23207-117">-SubscriptionId</span></span>
<span data-ttu-id="23207-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="23207-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="23207-119">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="23207-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23207-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23207-120">CommonParameters</span></span>
<span data-ttu-id="23207-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23207-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23207-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23207-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23207-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23207-123">INPUTS</span></span>

## <span data-ttu-id="23207-124">輸出</span><span class="sxs-lookup"><span data-stu-id="23207-124">OUTPUTS</span></span>

### <span data-ttu-id="23207-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="23207-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="23207-126">筆記</span><span class="sxs-lookup"><span data-stu-id="23207-126">NOTES</span></span>

<span data-ttu-id="23207-127">別名</span><span class="sxs-lookup"><span data-stu-id="23207-127">ALIASES</span></span>

## <span data-ttu-id="23207-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="23207-128">RELATED LINKS</span></span>

