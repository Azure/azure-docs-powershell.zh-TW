---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286227"
---
# <span data-ttu-id="12924-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="12924-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="12924-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12924-102">SYNOPSIS</span></span>
<span data-ttu-id="12924-103">用來顯示訂閱之資源間的允許流量</span><span class="sxs-lookup"><span data-stu-id="12924-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="12924-104">句法</span><span class="sxs-lookup"><span data-stu-id="12924-104">SYNTAX</span></span>

### <span data-ttu-id="12924-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="12924-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12924-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="12924-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12924-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12924-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12924-108">說明</span><span class="sxs-lookup"><span data-stu-id="12924-108">DESCRIPTION</span></span>
<span data-ttu-id="12924-109">根據連線類型，取得訂閱和位置之資源間所有可能流量的清單。</span><span class="sxs-lookup"><span data-stu-id="12924-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="12924-110">示例</span><span class="sxs-lookup"><span data-stu-id="12924-110">EXAMPLES</span></span>

### <span data-ttu-id="12924-111">範例1</span><span class="sxs-lookup"><span data-stu-id="12924-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="12924-112">範例2</span><span class="sxs-lookup"><span data-stu-id="12924-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="12924-113">根據連線類型，取得訂閱和位置之資源間所有可能流量的清單。</span><span class="sxs-lookup"><span data-stu-id="12924-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="12924-114">參數</span><span class="sxs-lookup"><span data-stu-id="12924-114">PARAMETERS</span></span>

### <span data-ttu-id="12924-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12924-115">-DefaultProfile</span></span>
<span data-ttu-id="12924-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12924-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12924-117">-位置</span><span class="sxs-lookup"><span data-stu-id="12924-117">-Location</span></span>
<span data-ttu-id="12924-118">位於.</span><span class="sxs-lookup"><span data-stu-id="12924-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12924-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="12924-119">-Name</span></span>
<span data-ttu-id="12924-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="12924-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12924-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12924-121">-ResourceGroupName</span></span>
<span data-ttu-id="12924-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="12924-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12924-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12924-123">-ResourceId</span></span>
<span data-ttu-id="12924-124">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="12924-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12924-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12924-125">CommonParameters</span></span>
<span data-ttu-id="12924-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12924-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12924-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12924-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12924-128">輸入</span><span class="sxs-lookup"><span data-stu-id="12924-128">INPUTS</span></span>

### <span data-ttu-id="12924-129">System.object</span><span class="sxs-lookup"><span data-stu-id="12924-129">System.String</span></span>

## <span data-ttu-id="12924-130">輸出</span><span class="sxs-lookup"><span data-stu-id="12924-130">OUTPUTS</span></span>

### <span data-ttu-id="12924-131">PSSecurityAllowedConnection 中的 AllowedConnection （Security..。</span><span class="sxs-lookup"><span data-stu-id="12924-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="12924-132">筆記</span><span class="sxs-lookup"><span data-stu-id="12924-132">NOTES</span></span>

## <span data-ttu-id="12924-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="12924-133">RELATED LINKS</span></span>
