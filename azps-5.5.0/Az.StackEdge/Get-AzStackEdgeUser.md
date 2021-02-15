---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130626"
---
# <span data-ttu-id="60687-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="60687-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="60687-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60687-102">SYNOPSIS</span></span>
<span data-ttu-id="60687-103">取得裝置的已設定使用者。</span><span class="sxs-lookup"><span data-stu-id="60687-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="60687-104">句法</span><span class="sxs-lookup"><span data-stu-id="60687-104">SYNTAX</span></span>

### <span data-ttu-id="60687-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60687-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60687-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60687-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60687-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60687-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60687-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60687-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="60687-109">說明</span><span class="sxs-lookup"><span data-stu-id="60687-109">DESCRIPTION</span></span>
<span data-ttu-id="60687-110">**AzStackEdgeUser** Cmdlet 會列出針對堆疊 Edge 裝置設定的使用者。</span><span class="sxs-lookup"><span data-stu-id="60687-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="60687-111">您可以在 [參數] 中提及名稱，以取得特定使用者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="60687-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="60687-112">示例</span><span class="sxs-lookup"><span data-stu-id="60687-112">EXAMPLES</span></span>

### <span data-ttu-id="60687-113">範例1</span><span class="sxs-lookup"><span data-stu-id="60687-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="60687-114">參數</span><span class="sxs-lookup"><span data-stu-id="60687-114">PARAMETERS</span></span>

### <span data-ttu-id="60687-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60687-115">-DefaultProfile</span></span>
<span data-ttu-id="60687-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60687-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60687-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="60687-117">-DeviceName</span></span>
<span data-ttu-id="60687-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="60687-118">Device Name</span></span>

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

### <span data-ttu-id="60687-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="60687-119">-DeviceObject</span></span>
<span data-ttu-id="60687-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="60687-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="60687-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="60687-121">-Name</span></span>
<span data-ttu-id="60687-122">Username</span><span class="sxs-lookup"><span data-stu-id="60687-122">Username</span></span>

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

### <span data-ttu-id="60687-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60687-123">-ResourceGroupName</span></span>
<span data-ttu-id="60687-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="60687-124">Resource Group Name</span></span>

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

### <span data-ttu-id="60687-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60687-125">-ResourceId</span></span>
<span data-ttu-id="60687-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="60687-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="60687-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60687-127">CommonParameters</span></span>
<span data-ttu-id="60687-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60687-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60687-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60687-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60687-130">輸入</span><span class="sxs-lookup"><span data-stu-id="60687-130">INPUTS</span></span>

### <span data-ttu-id="60687-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="60687-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="60687-132">輸出</span><span class="sxs-lookup"><span data-stu-id="60687-132">OUTPUTS</span></span>

### <span data-ttu-id="60687-133">PSStackEdgeUser （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="60687-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="60687-134">筆記</span><span class="sxs-lookup"><span data-stu-id="60687-134">NOTES</span></span>

## <span data-ttu-id="60687-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="60687-135">RELATED LINKS</span></span>
