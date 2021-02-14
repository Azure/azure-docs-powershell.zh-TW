---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143326"
---
# <span data-ttu-id="135ef-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="135ef-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="135ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="135ef-102">SYNOPSIS</span></span>
<span data-ttu-id="135ef-103">取得延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="135ef-103">The operation to get the extension.</span></span>

## <span data-ttu-id="135ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="135ef-104">SYNTAX</span></span>

### <span data-ttu-id="135ef-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="135ef-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="135ef-106">獲取</span><span class="sxs-lookup"><span data-stu-id="135ef-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="135ef-107">說明</span><span class="sxs-lookup"><span data-stu-id="135ef-107">DESCRIPTION</span></span>
<span data-ttu-id="135ef-108">取得延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="135ef-108">The operation to get the extension.</span></span>

## <span data-ttu-id="135ef-109">示例</span><span class="sxs-lookup"><span data-stu-id="135ef-109">EXAMPLES</span></span>

### <span data-ttu-id="135ef-110">範例1：列出電腦的所有擴充功能</span><span class="sxs-lookup"><span data-stu-id="135ef-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="135ef-111">列出特定電腦的所有延伸。</span><span class="sxs-lookup"><span data-stu-id="135ef-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="135ef-112">範例2：在電腦上取得特定副檔名</span><span class="sxs-lookup"><span data-stu-id="135ef-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="135ef-113">取得電腦上的特定延伸。</span><span class="sxs-lookup"><span data-stu-id="135ef-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="135ef-114">參數</span><span class="sxs-lookup"><span data-stu-id="135ef-114">PARAMETERS</span></span>

### <span data-ttu-id="135ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135ef-115">-DefaultProfile</span></span>
<span data-ttu-id="135ef-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="135ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="135ef-117">-展開</span><span class="sxs-lookup"><span data-stu-id="135ef-117">-Expand</span></span>
<span data-ttu-id="135ef-118">要套用在運算上的 expand 運算式。</span><span class="sxs-lookup"><span data-stu-id="135ef-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ef-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="135ef-119">-MachineName</span></span>
<span data-ttu-id="135ef-120">包含副檔名的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="135ef-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="135ef-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="135ef-121">-Name</span></span>
<span data-ttu-id="135ef-122">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="135ef-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="135ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="135ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="135ef-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="135ef-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="135ef-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="135ef-125">-SubscriptionId</span></span>
<span data-ttu-id="135ef-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="135ef-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="135ef-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="135ef-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="135ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135ef-128">CommonParameters</span></span>
<span data-ttu-id="135ef-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="135ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135ef-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="135ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135ef-131">輸入</span><span class="sxs-lookup"><span data-stu-id="135ef-131">INPUTS</span></span>

## <span data-ttu-id="135ef-132">輸出</span><span class="sxs-lookup"><span data-stu-id="135ef-132">OUTPUTS</span></span>

### <span data-ttu-id="135ef-133">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="135ef-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="135ef-134">筆記</span><span class="sxs-lookup"><span data-stu-id="135ef-134">NOTES</span></span>

<span data-ttu-id="135ef-135">別名</span><span class="sxs-lookup"><span data-stu-id="135ef-135">ALIASES</span></span>

## <span data-ttu-id="135ef-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="135ef-136">RELATED LINKS</span></span>

