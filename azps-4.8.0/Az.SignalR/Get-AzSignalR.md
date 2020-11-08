---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129889"
---
# <span data-ttu-id="37600-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="37600-101">Get-AzSignalR</span></span>

## <span data-ttu-id="37600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37600-102">SYNOPSIS</span></span>
<span data-ttu-id="37600-103">取得資源群組或訂閱中的特定 SignalR 服務或所有 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="37600-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="37600-104">句法</span><span class="sxs-lookup"><span data-stu-id="37600-104">SYNTAX</span></span>

### <span data-ttu-id="37600-105">ListSignalRServiceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37600-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37600-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="37600-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37600-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37600-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37600-108">說明</span><span class="sxs-lookup"><span data-stu-id="37600-108">DESCRIPTION</span></span>
<span data-ttu-id="37600-109">取得資源群組或訂閱中的特定 SignalR 服務或所有 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="37600-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="37600-110">示例</span><span class="sxs-lookup"><span data-stu-id="37600-110">EXAMPLES</span></span>

### <span data-ttu-id="37600-111">取得訂閱中的所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="37600-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="37600-112">取得資源群組中的所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="37600-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="37600-113">取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="37600-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="37600-114">從預設資源群組取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="37600-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="37600-115">預設的資源群組可以由 \` AzDefault-ResourceGroupName myResourceGroup 進行設定 \` 。</span><span class="sxs-lookup"><span data-stu-id="37600-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="37600-116">參數</span><span class="sxs-lookup"><span data-stu-id="37600-116">PARAMETERS</span></span>

### <span data-ttu-id="37600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37600-117">-DefaultProfile</span></span>
<span data-ttu-id="37600-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37600-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37600-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="37600-119">-Name</span></span>
<span data-ttu-id="37600-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="37600-120">SignalR service name.</span></span>

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

### <span data-ttu-id="37600-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37600-121">-ResourceGroupName</span></span>
<span data-ttu-id="37600-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="37600-122">Resource group name.</span></span>

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

### <span data-ttu-id="37600-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37600-123">-ResourceId</span></span>
<span data-ttu-id="37600-124">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37600-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="37600-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37600-125">CommonParameters</span></span>
<span data-ttu-id="37600-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37600-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37600-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37600-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37600-128">輸入</span><span class="sxs-lookup"><span data-stu-id="37600-128">INPUTS</span></span>

### <span data-ttu-id="37600-129">System.object</span><span class="sxs-lookup"><span data-stu-id="37600-129">System.String</span></span>
## <span data-ttu-id="37600-130">輸出</span><span class="sxs-lookup"><span data-stu-id="37600-130">OUTPUTS</span></span>

### <span data-ttu-id="37600-131">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="37600-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="37600-132">筆記</span><span class="sxs-lookup"><span data-stu-id="37600-132">NOTES</span></span>

## <span data-ttu-id="37600-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="37600-133">RELATED LINKS</span></span>