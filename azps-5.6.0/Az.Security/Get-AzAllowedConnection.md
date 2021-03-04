---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 211601ac2866dab85d46e61cba79ed074f79e22d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906418"
---
# <span data-ttu-id="e6904-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="e6904-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="e6904-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6904-102">SYNOPSIS</span></span>
<span data-ttu-id="e6904-103">用來顯示訂閱資源之間的允許流量</span><span class="sxs-lookup"><span data-stu-id="e6904-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="e6904-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6904-104">SYNTAX</span></span>

### <span data-ttu-id="e6904-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="e6904-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6904-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e6904-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6904-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6904-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6904-108">描述</span><span class="sxs-lookup"><span data-stu-id="e6904-108">DESCRIPTION</span></span>
<span data-ttu-id="e6904-109">根據連線類型，在訂閱的資源與位置之間，獲得所有可能的流量清單。</span><span class="sxs-lookup"><span data-stu-id="e6904-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="e6904-110">例子</span><span class="sxs-lookup"><span data-stu-id="e6904-110">EXAMPLES</span></span>

### <span data-ttu-id="e6904-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e6904-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="e6904-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e6904-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e6904-113">根據連線類型，在訂閱的資源與位置之間，獲得所有可能的流量清單。</span><span class="sxs-lookup"><span data-stu-id="e6904-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="e6904-114">參數</span><span class="sxs-lookup"><span data-stu-id="e6904-114">PARAMETERS</span></span>

### <span data-ttu-id="e6904-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6904-115">-DefaultProfile</span></span>
<span data-ttu-id="e6904-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6904-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6904-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e6904-117">-Location</span></span>
<span data-ttu-id="e6904-118">位置。</span><span class="sxs-lookup"><span data-stu-id="e6904-118">Location.</span></span>

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

### <span data-ttu-id="e6904-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6904-119">-Name</span></span>
<span data-ttu-id="e6904-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e6904-120">Resource name.</span></span>

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

### <span data-ttu-id="e6904-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6904-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6904-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e6904-122">Resource group name.</span></span>

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

### <span data-ttu-id="e6904-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6904-123">-ResourceId</span></span>
<span data-ttu-id="e6904-124">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6904-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e6904-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6904-125">CommonParameters</span></span>
<span data-ttu-id="e6904-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6904-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6904-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e6904-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6904-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e6904-128">INPUTS</span></span>

### <span data-ttu-id="e6904-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e6904-129">System.String</span></span>

## <span data-ttu-id="e6904-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e6904-130">OUTPUTS</span></span>

### <span data-ttu-id="e6904-131">Microsoft.Azure.Commands.Security.models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="e6904-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="e6904-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e6904-132">NOTES</span></span>

## <span data-ttu-id="e6904-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6904-133">RELATED LINKS</span></span>
