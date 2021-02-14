---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129911"
---
# <span data-ttu-id="b9c1b-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="b9c1b-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="b9c1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c1b-103">檢索雲端服務中角色實例之執行時間狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="b9c1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9c1b-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9c1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c1b-106">檢索雲端服務中角色實例之執行時間狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="b9c1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="b9c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c1b-108">範例1：取得雲端服務角色實例的實例視圖詳細資料</span><span class="sxs-lookup"><span data-stu-id="b9c1b-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="b9c1b-109">這個 Cmdlet 會從屬於名為 ContosOrg 之資源群組的名為 ContosoCS 的雲端服務，取得 ContosoFrontEnd_IN_0 名為「」的角色實例的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b9c1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c1b-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b9c1b-111">-CloudServiceName</span></span>
<span data-ttu-id="b9c1b-112">.</span><span class="sxs-lookup"><span data-stu-id="b9c1b-112">.</span></span>

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

### <span data-ttu-id="b9c1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c1b-113">-DefaultProfile</span></span>
<span data-ttu-id="b9c1b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c1b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c1b-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9c1b-116">.</span><span class="sxs-lookup"><span data-stu-id="b9c1b-116">.</span></span>

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

### <span data-ttu-id="b9c1b-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="b9c1b-117">-RoleInstanceName</span></span>
<span data-ttu-id="b9c1b-118">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="b9c1b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9c1b-119">-SubscriptionId</span></span>
<span data-ttu-id="b9c1b-120">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9c1b-121">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9c1b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c1b-122">CommonParameters</span></span>
<span data-ttu-id="b9c1b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c1b-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c1b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b9c1b-125">INPUTS</span></span>

## <span data-ttu-id="b9c1b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b9c1b-126">OUTPUTS</span></span>

### <span data-ttu-id="b9c1b-127">IRoleInstanceView （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="b9c1b-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="b9c1b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b9c1b-128">NOTES</span></span>

<span data-ttu-id="b9c1b-129">別名</span><span class="sxs-lookup"><span data-stu-id="b9c1b-129">ALIASES</span></span>

## <span data-ttu-id="b9c1b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9c1b-130">RELATED LINKS</span></span>

