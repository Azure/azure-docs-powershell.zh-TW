---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902798"
---
# <span data-ttu-id="9382f-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="9382f-101">Get-AzSignalR</span></span>

## <span data-ttu-id="9382f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9382f-102">SYNOPSIS</span></span>
<span data-ttu-id="9382f-103">取得特定 SignalR 服務或資源群組或訂閱中所有的 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="9382f-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="9382f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9382f-104">SYNTAX</span></span>

### <span data-ttu-id="9382f-105">ListSignalRServiceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9382f-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9382f-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9382f-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9382f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9382f-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9382f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9382f-108">DESCRIPTION</span></span>
<span data-ttu-id="9382f-109">取得特定 SignalR 服務或資源群組或訂閱中所有的 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="9382f-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="9382f-110">例子</span><span class="sxs-lookup"><span data-stu-id="9382f-110">EXAMPLES</span></span>

### <span data-ttu-id="9382f-111">取得訂閱中所有的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="9382f-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="9382f-112">取得資源群組中所有的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="9382f-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="9382f-113">取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="9382f-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="9382f-114">從預設資源群組取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="9382f-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="9382f-115">預設資源群組可以設定為 \` Set-AzDefault -ResourceGroupName myResourceGroup。 \`</span><span class="sxs-lookup"><span data-stu-id="9382f-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="9382f-116">參數</span><span class="sxs-lookup"><span data-stu-id="9382f-116">PARAMETERS</span></span>

### <span data-ttu-id="9382f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9382f-117">-DefaultProfile</span></span>
<span data-ttu-id="9382f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9382f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9382f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9382f-119">-Name</span></span>
<span data-ttu-id="9382f-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="9382f-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9382f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9382f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9382f-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9382f-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9382f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9382f-123">-ResourceId</span></span>
<span data-ttu-id="9382f-124">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9382f-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9382f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9382f-125">CommonParameters</span></span>
<span data-ttu-id="9382f-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9382f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9382f-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9382f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9382f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9382f-128">INPUTS</span></span>

### <span data-ttu-id="9382f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9382f-129">System.String</span></span>
## <span data-ttu-id="9382f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9382f-130">OUTPUTS</span></span>

### <span data-ttu-id="9382f-131">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="9382f-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="9382f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9382f-132">NOTES</span></span>

## <span data-ttu-id="9382f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9382f-133">RELATED LINKS</span></span>
