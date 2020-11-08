---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971162"
---
# <span data-ttu-id="29ac7-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="29ac7-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="29ac7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="29ac7-103">取得裝置的已設定使用者。</span><span class="sxs-lookup"><span data-stu-id="29ac7-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="29ac7-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ac7-104">SYNTAX</span></span>

### <span data-ttu-id="29ac7-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29ac7-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ac7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ac7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ac7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ac7-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29ac7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29ac7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="29ac7-109">說明</span><span class="sxs-lookup"><span data-stu-id="29ac7-109">DESCRIPTION</span></span>
<span data-ttu-id="29ac7-110">**AzDataBoxEdgeUser** Cmdlet 會列出針對資料編輯方塊邊緣裝置設定的使用者。</span><span class="sxs-lookup"><span data-stu-id="29ac7-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="29ac7-111">您可以在 [參數] 中提及名稱，以取得特定使用者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="29ac7-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="29ac7-112">示例</span><span class="sxs-lookup"><span data-stu-id="29ac7-112">EXAMPLES</span></span>

### <span data-ttu-id="29ac7-113">範例1</span><span class="sxs-lookup"><span data-stu-id="29ac7-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="29ac7-114">參數</span><span class="sxs-lookup"><span data-stu-id="29ac7-114">PARAMETERS</span></span>

### <span data-ttu-id="29ac7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ac7-115">-DefaultProfile</span></span>
<span data-ttu-id="29ac7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29ac7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29ac7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="29ac7-117">-DeviceName</span></span>
<span data-ttu-id="29ac7-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="29ac7-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ac7-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="29ac7-119">-DeviceObject</span></span>
<span data-ttu-id="29ac7-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="29ac7-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29ac7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="29ac7-121">-Name</span></span>
<span data-ttu-id="29ac7-122">Username</span><span class="sxs-lookup"><span data-stu-id="29ac7-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ac7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ac7-123">-ResourceGroupName</span></span>
<span data-ttu-id="29ac7-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="29ac7-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ac7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ac7-125">-ResourceId</span></span>
<span data-ttu-id="29ac7-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ac7-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ac7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ac7-127">CommonParameters</span></span>
<span data-ttu-id="29ac7-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ac7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ac7-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29ac7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ac7-130">輸入</span><span class="sxs-lookup"><span data-stu-id="29ac7-130">INPUTS</span></span>

### <span data-ttu-id="29ac7-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="29ac7-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="29ac7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="29ac7-132">OUTPUTS</span></span>

### <span data-ttu-id="29ac7-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="29ac7-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="29ac7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="29ac7-134">NOTES</span></span>

## <span data-ttu-id="29ac7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ac7-135">RELATED LINKS</span></span>
