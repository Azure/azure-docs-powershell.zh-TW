---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916434"
---
# <span data-ttu-id="ce50e-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="ce50e-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="ce50e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce50e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce50e-103">在雲端服務中，取回角色實例的執行時間狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ce50e-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="ce50e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce50e-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ce50e-105">描述</span><span class="sxs-lookup"><span data-stu-id="ce50e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce50e-106">在雲端服務中，取回角色實例的執行時間狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ce50e-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="ce50e-107">例子</span><span class="sxs-lookup"><span data-stu-id="ce50e-107">EXAMPLES</span></span>

### <span data-ttu-id="ce50e-108">範例 1：取得雲端服務角色實例的實例視圖詳細資料</span><span class="sxs-lookup"><span data-stu-id="ce50e-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="ce50e-109">此 Cmdlet 會獲得名為 contosoCS 之雲端服務 ContosoFrontEnd_IN_0 名稱之角色實例的實例視圖，該角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ce50e-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="ce50e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce50e-110">PARAMETERS</span></span>

### <span data-ttu-id="ce50e-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ce50e-111">-CloudServiceName</span></span>
<span data-ttu-id="ce50e-112">.</span><span class="sxs-lookup"><span data-stu-id="ce50e-112">.</span></span>

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

### <span data-ttu-id="ce50e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce50e-113">-DefaultProfile</span></span>
<span data-ttu-id="ce50e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce50e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce50e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce50e-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce50e-116">.</span><span class="sxs-lookup"><span data-stu-id="ce50e-116">.</span></span>

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

### <span data-ttu-id="ce50e-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="ce50e-117">-RoleInstanceName</span></span>
<span data-ttu-id="ce50e-118">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce50e-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="ce50e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce50e-119">-SubscriptionId</span></span>
<span data-ttu-id="ce50e-120">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ce50e-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce50e-121">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ce50e-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ce50e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce50e-122">CommonParameters</span></span>
<span data-ttu-id="ce50e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce50e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce50e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce50e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce50e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ce50e-125">INPUTS</span></span>

## <span data-ttu-id="ce50e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ce50e-126">OUTPUTS</span></span>

### <span data-ttu-id="ce50e-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="ce50e-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="ce50e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ce50e-128">NOTES</span></span>

<span data-ttu-id="ce50e-129">別名</span><span class="sxs-lookup"><span data-stu-id="ce50e-129">ALIASES</span></span>

## <span data-ttu-id="ce50e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce50e-130">RELATED LINKS</span></span>

