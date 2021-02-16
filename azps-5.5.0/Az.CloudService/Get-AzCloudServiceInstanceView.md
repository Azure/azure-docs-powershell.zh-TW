---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139391"
---
# <span data-ttu-id="a0cb8-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="a0cb8-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="a0cb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cb8-103">取得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="a0cb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0cb8-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a0cb8-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cb8-106">取得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="a0cb8-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="a0cb8-108">範例1：取得雲端服務實例視圖</span><span class="sxs-lookup"><span data-stu-id="a0cb8-108">Example 1: Get cloud service instance view</span></span>
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

<span data-ttu-id="a0cb8-109">這個 Cmdlet 會取得屬於名為 ContosOrg 之資源群組之名為 ContosoCS 之雲端服務的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a0cb8-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0cb8-110">PARAMETERS</span></span>

### <span data-ttu-id="a0cb8-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a0cb8-111">-CloudServiceName</span></span>
<span data-ttu-id="a0cb8-112">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="a0cb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cb8-113">-DefaultProfile</span></span>
<span data-ttu-id="a0cb8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0cb8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cb8-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0cb8-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="a0cb8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0cb8-117">-SubscriptionId</span></span>
<span data-ttu-id="a0cb8-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0cb8-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0cb8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cb8-120">CommonParameters</span></span>
<span data-ttu-id="a0cb8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cb8-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cb8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a0cb8-123">INPUTS</span></span>

## <span data-ttu-id="a0cb8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a0cb8-124">OUTPUTS</span></span>

### <span data-ttu-id="a0cb8-125">ICloudServiceInstanceView （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="a0cb8-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="a0cb8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a0cb8-126">NOTES</span></span>

<span data-ttu-id="a0cb8-127">別名</span><span class="sxs-lookup"><span data-stu-id="a0cb8-127">ALIASES</span></span>

## <span data-ttu-id="a0cb8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0cb8-128">RELATED LINKS</span></span>

