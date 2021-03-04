---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 9d06873954e6a6880965781d2004d8b7b0c35bb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908333"
---
# <span data-ttu-id="1127c-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1127c-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="1127c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1127c-102">SYNOPSIS</span></span>
<span data-ttu-id="1127c-103">為裝置獲得已配置的使用者。</span><span class="sxs-lookup"><span data-stu-id="1127c-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="1127c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1127c-104">SYNTAX</span></span>

### <span data-ttu-id="1127c-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1127c-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1127c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1127c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1127c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1127c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1127c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1127c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1127c-109">描述</span><span class="sxs-lookup"><span data-stu-id="1127c-109">DESCRIPTION</span></span>
<span data-ttu-id="1127c-110">**Get-AzStackEdgeUser** Cmdlet 會列出為 Stack Edge 裝置所配置的使用者。</span><span class="sxs-lookup"><span data-stu-id="1127c-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="1127c-111">您可以在參數中提及名稱，以取得特定使用者的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1127c-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="1127c-112">例子</span><span class="sxs-lookup"><span data-stu-id="1127c-112">EXAMPLES</span></span>

### <span data-ttu-id="1127c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="1127c-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="1127c-114">參數</span><span class="sxs-lookup"><span data-stu-id="1127c-114">PARAMETERS</span></span>

### <span data-ttu-id="1127c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1127c-115">-DefaultProfile</span></span>
<span data-ttu-id="1127c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1127c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1127c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1127c-117">-DeviceName</span></span>
<span data-ttu-id="1127c-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="1127c-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1127c-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="1127c-119">-DeviceObject</span></span>
<span data-ttu-id="1127c-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="1127c-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1127c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1127c-121">-Name</span></span>
<span data-ttu-id="1127c-122">使用者</span><span class="sxs-lookup"><span data-stu-id="1127c-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1127c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1127c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1127c-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="1127c-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1127c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1127c-125">-ResourceId</span></span>
<span data-ttu-id="1127c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1127c-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1127c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1127c-127">CommonParameters</span></span>
<span data-ttu-id="1127c-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1127c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1127c-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1127c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1127c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1127c-130">INPUTS</span></span>

### <span data-ttu-id="1127c-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1127c-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="1127c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1127c-132">OUTPUTS</span></span>

### <span data-ttu-id="1127c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1127c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="1127c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1127c-134">NOTES</span></span>

## <span data-ttu-id="1127c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1127c-135">RELATED LINKS</span></span>
