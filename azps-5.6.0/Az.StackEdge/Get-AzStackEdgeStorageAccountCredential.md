---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: efb9c7828417596afecc21fc5e5c2b2b8f7c81b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916346"
---
# <span data-ttu-id="76aa0-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="76aa0-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="76aa0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="76aa0-103">獲得與裝置上儲存帳戶對應的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="76aa0-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="76aa0-104">語法</span><span class="sxs-lookup"><span data-stu-id="76aa0-104">SYNTAX</span></span>

### <span data-ttu-id="76aa0-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76aa0-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76aa0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76aa0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76aa0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76aa0-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76aa0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76aa0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="76aa0-109">描述</span><span class="sxs-lookup"><span data-stu-id="76aa0-109">DESCRIPTION</span></span>
<span data-ttu-id="76aa0-110">**Get-AzStackEdgeStorageAccountCredential Cmdlet** 會取得 Stack Edge 裝置上對應儲存帳戶的儲存帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="76aa0-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="76aa0-111">您可以指定名稱、資源組名及裝置名稱參數，以取得特定儲存帳號憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="76aa0-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="76aa0-112">例子</span><span class="sxs-lookup"><span data-stu-id="76aa0-112">EXAMPLES</span></span>

### <span data-ttu-id="76aa0-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="76aa0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="76aa0-114">參數</span><span class="sxs-lookup"><span data-stu-id="76aa0-114">PARAMETERS</span></span>

### <span data-ttu-id="76aa0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aa0-115">-DefaultProfile</span></span>
<span data-ttu-id="76aa0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76aa0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76aa0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="76aa0-117">-DeviceName</span></span>
<span data-ttu-id="76aa0-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="76aa0-118">Device Name</span></span>

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

### <span data-ttu-id="76aa0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="76aa0-119">-DeviceObject</span></span>
<span data-ttu-id="76aa0-120">請提供對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="76aa0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="76aa0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="76aa0-121">-Name</span></span>
<span data-ttu-id="76aa0-122">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="76aa0-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76aa0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76aa0-123">-ResourceGroupName</span></span>
<span data-ttu-id="76aa0-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="76aa0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="76aa0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76aa0-125">-ResourceId</span></span>
<span data-ttu-id="76aa0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="76aa0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="76aa0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aa0-127">CommonParameters</span></span>
<span data-ttu-id="76aa0-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76aa0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aa0-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76aa0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aa0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="76aa0-130">INPUTS</span></span>

### <span data-ttu-id="76aa0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="76aa0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="76aa0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="76aa0-132">OUTPUTS</span></span>

### <span data-ttu-id="76aa0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="76aa0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="76aa0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="76aa0-134">NOTES</span></span>

## <span data-ttu-id="76aa0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="76aa0-135">RELATED LINKS</span></span>
