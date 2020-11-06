---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449723"
---
# <span data-ttu-id="82e48-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="82e48-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="82e48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82e48-102">SYNOPSIS</span></span>
<span data-ttu-id="82e48-103">取得資源群組或訂閱中的特定 SignalR 服務或所有 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="82e48-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82e48-104">句法</span><span class="sxs-lookup"><span data-stu-id="82e48-104">SYNTAX</span></span>

### <span data-ttu-id="82e48-105">ListSignalRServiceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="82e48-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82e48-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e48-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82e48-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e48-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e48-108">說明</span><span class="sxs-lookup"><span data-stu-id="82e48-108">DESCRIPTION</span></span>
<span data-ttu-id="82e48-109">取得資源群組或訂閱中的特定 SignalR 服務或所有 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="82e48-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="82e48-110">示例</span><span class="sxs-lookup"><span data-stu-id="82e48-110">EXAMPLES</span></span>

### <span data-ttu-id="82e48-111">取得訂閱中的所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="82e48-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="82e48-112">取得資源群組中的所有 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="82e48-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="82e48-113">取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="82e48-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="82e48-114">從預設資源群組取得特定的 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="82e48-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="82e48-115">預設的資源群組可以由設定 `Set-AzureRmDefault -ResourceGroupName myResourceGroup` 。</span><span class="sxs-lookup"><span data-stu-id="82e48-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="82e48-116">參數</span><span class="sxs-lookup"><span data-stu-id="82e48-116">PARAMETERS</span></span>

### <span data-ttu-id="82e48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e48-117">-DefaultProfile</span></span>
<span data-ttu-id="82e48-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82e48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e48-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="82e48-119">-Name</span></span>
<span data-ttu-id="82e48-120">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="82e48-120">SignalR service name.</span></span>

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

### <span data-ttu-id="82e48-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e48-121">-ResourceGroupName</span></span>
<span data-ttu-id="82e48-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="82e48-122">Resource group name.</span></span>

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

### <span data-ttu-id="82e48-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82e48-123">-ResourceId</span></span>
<span data-ttu-id="82e48-124">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82e48-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="82e48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e48-125">CommonParameters</span></span>
<span data-ttu-id="82e48-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82e48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e48-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82e48-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e48-128">輸入</span><span class="sxs-lookup"><span data-stu-id="82e48-128">INPUTS</span></span>

### <span data-ttu-id="82e48-129">System.object</span><span class="sxs-lookup"><span data-stu-id="82e48-129">System.String</span></span>
<span data-ttu-id="82e48-130">參數： ResourceId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="82e48-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="82e48-131">輸出</span><span class="sxs-lookup"><span data-stu-id="82e48-131">OUTPUTS</span></span>

### <span data-ttu-id="82e48-132">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="82e48-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="82e48-133">筆記</span><span class="sxs-lookup"><span data-stu-id="82e48-133">NOTES</span></span>

## <span data-ttu-id="82e48-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="82e48-134">RELATED LINKS</span></span>
