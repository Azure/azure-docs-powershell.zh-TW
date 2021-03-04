---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: b4dbee18ef0fad33180e9cc9c3d04a49e1288b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907214"
---
# <span data-ttu-id="6764f-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="6764f-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="6764f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6764f-102">SYNOPSIS</span></span>
<span data-ttu-id="6764f-103">此命令會列出特定同步處理群組內的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="6764f-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="6764f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6764f-104">SYNTAX</span></span>

### <span data-ttu-id="6764f-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6764f-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6764f-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6764f-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6764f-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6764f-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6764f-108">描述</span><span class="sxs-lookup"><span data-stu-id="6764f-108">DESCRIPTION</span></span>
<span data-ttu-id="6764f-109">此命令會列出特定同步處理群組內的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="6764f-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="6764f-110">它可以用來列出每個雲端端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="6764f-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="6764f-111">例子</span><span class="sxs-lookup"><span data-stu-id="6764f-111">EXAMPLES</span></span>

### <span data-ttu-id="6764f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6764f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="6764f-113">此命令會獲得指定同步處理群組中包含的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="6764f-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="6764f-114">指定 -CloudEndpointName 以返回特定名稱。</span><span class="sxs-lookup"><span data-stu-id="6764f-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="6764f-115">參數</span><span class="sxs-lookup"><span data-stu-id="6764f-115">PARAMETERS</span></span>

### <span data-ttu-id="6764f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6764f-116">-DefaultProfile</span></span>
<span data-ttu-id="6764f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6764f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6764f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6764f-118">-Name</span></span>
<span data-ttu-id="6764f-119">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6764f-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6764f-120">-ParentObject</span></span>
<span data-ttu-id="6764f-121">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="6764f-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6764f-122">-ParentResourceId</span></span>
<span data-ttu-id="6764f-123">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="6764f-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6764f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6764f-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6764f-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6764f-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="6764f-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6764f-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6764f-128">-SyncGroupName</span></span>
<span data-ttu-id="6764f-129">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6764f-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6764f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6764f-130">CommonParameters</span></span>
<span data-ttu-id="6764f-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6764f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6764f-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6764f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6764f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6764f-133">INPUTS</span></span>

### <span data-ttu-id="6764f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6764f-134">System.String</span></span>

### <span data-ttu-id="6764f-135">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6764f-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="6764f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6764f-136">OUTPUTS</span></span>

### <span data-ttu-id="6764f-137">Microsoft.Azure.Commands.StorageSync.models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="6764f-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="6764f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6764f-138">NOTES</span></span>

## <span data-ttu-id="6764f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6764f-139">RELATED LINKS</span></span>
