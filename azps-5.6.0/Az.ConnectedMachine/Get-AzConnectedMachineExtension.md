---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917022"
---
# <span data-ttu-id="d7873-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d7873-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d7873-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7873-102">SYNOPSIS</span></span>
<span data-ttu-id="d7873-103">取得擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="d7873-103">The operation to get the extension.</span></span>

## <span data-ttu-id="d7873-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7873-104">SYNTAX</span></span>

### <span data-ttu-id="d7873-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="d7873-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7873-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d7873-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7873-107">描述</span><span class="sxs-lookup"><span data-stu-id="d7873-107">DESCRIPTION</span></span>
<span data-ttu-id="d7873-108">取得擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="d7873-108">The operation to get the extension.</span></span>

## <span data-ttu-id="d7873-109">例子</span><span class="sxs-lookup"><span data-stu-id="d7873-109">EXAMPLES</span></span>

### <span data-ttu-id="d7873-110">範例 1：列出電腦的所有延伸模組</span><span class="sxs-lookup"><span data-stu-id="d7873-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="d7873-111">列出特定電腦的所有擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d7873-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="d7873-112">範例 2：取得電腦上特定的擴充功能</span><span class="sxs-lookup"><span data-stu-id="d7873-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="d7873-113">在一部電腦上獲得特定的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d7873-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="d7873-114">參數</span><span class="sxs-lookup"><span data-stu-id="d7873-114">PARAMETERS</span></span>

### <span data-ttu-id="d7873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7873-115">-DefaultProfile</span></span>
<span data-ttu-id="d7873-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7873-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7873-117">-展開</span><span class="sxs-lookup"><span data-stu-id="d7873-117">-Expand</span></span>
<span data-ttu-id="d7873-118">要適用于作業的展開運算式。</span><span class="sxs-lookup"><span data-stu-id="d7873-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="d7873-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d7873-119">-MachineName</span></span>
<span data-ttu-id="d7873-120">包含副檔名的機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d7873-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="d7873-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7873-121">-Name</span></span>
<span data-ttu-id="d7873-122">電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="d7873-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="d7873-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7873-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7873-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7873-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7873-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7873-125">-SubscriptionId</span></span>
<span data-ttu-id="d7873-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d7873-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7873-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d7873-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d7873-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7873-128">CommonParameters</span></span>
<span data-ttu-id="d7873-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7873-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7873-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7873-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7873-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d7873-131">INPUTS</span></span>

## <span data-ttu-id="d7873-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d7873-132">OUTPUTS</span></span>

### <span data-ttu-id="d7873-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d7873-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d7873-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d7873-134">NOTES</span></span>

<span data-ttu-id="d7873-135">別名</span><span class="sxs-lookup"><span data-stu-id="d7873-135">ALIASES</span></span>

## <span data-ttu-id="d7873-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7873-136">RELATED LINKS</span></span>

