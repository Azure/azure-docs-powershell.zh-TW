---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 4bc1e887ba1f5fc9918c6b01858cf9bd2c116ca6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795774"
---
# <span data-ttu-id="487b1-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="487b1-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="487b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="487b1-102">SYNOPSIS</span></span>
<span data-ttu-id="487b1-103">取得與裝置上的儲存空間帳戶相對應的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="487b1-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="487b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="487b1-104">SYNTAX</span></span>

### <span data-ttu-id="487b1-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="487b1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="487b1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="487b1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="487b1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="487b1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="487b1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="487b1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="487b1-109">說明</span><span class="sxs-lookup"><span data-stu-id="487b1-109">DESCRIPTION</span></span>
<span data-ttu-id="487b1-110">**AzDataBoxEdgeStorageAccountCredential** Cmdlet 會取得資料盒 Edge 裝置上對應儲存空間帳戶的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="487b1-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="487b1-111">您可以指定名稱、資源群組名稱和裝置名稱參數，以取得特定儲存空間帳號憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="487b1-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="487b1-112">示例</span><span class="sxs-lookup"><span data-stu-id="487b1-112">EXAMPLES</span></span>

### <span data-ttu-id="487b1-113">範例1</span><span class="sxs-lookup"><span data-stu-id="487b1-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="487b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="487b1-114">PARAMETERS</span></span>

### <span data-ttu-id="487b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="487b1-115">-DefaultProfile</span></span>
<span data-ttu-id="487b1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="487b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="487b1-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="487b1-117">-DeviceName</span></span>
<span data-ttu-id="487b1-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="487b1-118">Device Name</span></span>

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

### <span data-ttu-id="487b1-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="487b1-119">-DeviceObject</span></span>
<span data-ttu-id="487b1-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="487b1-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="487b1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="487b1-121">-Name</span></span>
<span data-ttu-id="487b1-122">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="487b1-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="487b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="487b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="487b1-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="487b1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="487b1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="487b1-125">-ResourceId</span></span>
<span data-ttu-id="487b1-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="487b1-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="487b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487b1-127">CommonParameters</span></span>
<span data-ttu-id="487b1-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="487b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487b1-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="487b1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487b1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="487b1-130">INPUTS</span></span>

### <span data-ttu-id="487b1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="487b1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="487b1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="487b1-132">OUTPUTS</span></span>

### <span data-ttu-id="487b1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="487b1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="487b1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="487b1-134">NOTES</span></span>

## <span data-ttu-id="487b1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="487b1-135">RELATED LINKS</span></span>