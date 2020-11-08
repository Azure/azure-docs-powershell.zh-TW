---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971451"
---
# <span data-ttu-id="480f6-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="480f6-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="480f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="480f6-102">SYNOPSIS</span></span>
<span data-ttu-id="480f6-103">檢索 [模型視圖] 或混合式電腦的 [實例] 視圖的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="480f6-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="480f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="480f6-104">SYNTAX</span></span>

### <span data-ttu-id="480f6-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="480f6-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="480f6-106">獲取</span><span class="sxs-lookup"><span data-stu-id="480f6-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="480f6-107">清單</span><span class="sxs-lookup"><span data-stu-id="480f6-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="480f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="480f6-108">DESCRIPTION</span></span>
<span data-ttu-id="480f6-109">檢索 [模型視圖] 或混合式電腦的 [實例] 視圖的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="480f6-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="480f6-110">示例</span><span class="sxs-lookup"><span data-stu-id="480f6-110">EXAMPLES</span></span>

### <span data-ttu-id="480f6-111">範例1：列出訂閱中所有已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="480f6-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="480f6-112">列出訂閱中所有已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="480f6-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="480f6-113">如果未指定訂閱，它會從您目前的 Azure PowerShell 內容使用訂閱。</span><span class="sxs-lookup"><span data-stu-id="480f6-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="480f6-114">範例2：列出資源群組中所有已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="480f6-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="480f6-115">列出資源群組中所有已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="480f6-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="480f6-116">範例3：依名稱在資源群組中取得已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="480f6-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="480f6-117">依名稱在資源群組中取得已連線的電腦。</span><span class="sxs-lookup"><span data-stu-id="480f6-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="480f6-118">參數</span><span class="sxs-lookup"><span data-stu-id="480f6-118">PARAMETERS</span></span>

### <span data-ttu-id="480f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480f6-119">-DefaultProfile</span></span>
<span data-ttu-id="480f6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="480f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480f6-121">-展開</span><span class="sxs-lookup"><span data-stu-id="480f6-121">-Expand</span></span>
<span data-ttu-id="480f6-122">要套用在運算上的 expand 運算式。</span><span class="sxs-lookup"><span data-stu-id="480f6-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480f6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="480f6-123">-Name</span></span>
<span data-ttu-id="480f6-124">混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="480f6-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="480f6-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="480f6-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480f6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="480f6-127">-SubscriptionId</span></span>
<span data-ttu-id="480f6-128">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="480f6-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="480f6-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="480f6-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="480f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480f6-130">CommonParameters</span></span>
<span data-ttu-id="480f6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="480f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480f6-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="480f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480f6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="480f6-133">INPUTS</span></span>

## <span data-ttu-id="480f6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="480f6-134">OUTPUTS</span></span>

### <span data-ttu-id="480f6-135">IMachine （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="480f6-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="480f6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="480f6-136">NOTES</span></span>

<span data-ttu-id="480f6-137">別名</span><span class="sxs-lookup"><span data-stu-id="480f6-137">ALIASES</span></span>

## <span data-ttu-id="480f6-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="480f6-138">RELATED LINKS</span></span>
