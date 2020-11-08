---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126688"
---
# <span data-ttu-id="cf99a-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf99a-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="cf99a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf99a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf99a-103">這個命令會列出指定同步群組中的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="cf99a-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="cf99a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf99a-104">SYNTAX</span></span>

### <span data-ttu-id="cf99a-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf99a-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf99a-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf99a-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf99a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf99a-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf99a-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf99a-108">DESCRIPTION</span></span>
<span data-ttu-id="cf99a-109">這個命令會列出指定同步群組中的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="cf99a-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="cf99a-110">您也可以使用它來列出每個雲端端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf99a-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="cf99a-111">示例</span><span class="sxs-lookup"><span data-stu-id="cf99a-111">EXAMPLES</span></span>

### <span data-ttu-id="cf99a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="cf99a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="cf99a-113">這個命令會取得包含在指定同步群組中的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="cf99a-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="cf99a-114">指定-CloudEndpointName 以傳回特定的專案。</span><span class="sxs-lookup"><span data-stu-id="cf99a-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="cf99a-115">參數</span><span class="sxs-lookup"><span data-stu-id="cf99a-115">PARAMETERS</span></span>

### <span data-ttu-id="cf99a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf99a-116">-DefaultProfile</span></span>
<span data-ttu-id="cf99a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf99a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf99a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf99a-118">-Name</span></span>
<span data-ttu-id="cf99a-119">CloudEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf99a-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="cf99a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cf99a-120">-ParentObject</span></span>
<span data-ttu-id="cf99a-121">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="cf99a-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="cf99a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cf99a-122">-ParentResourceId</span></span>
<span data-ttu-id="cf99a-123">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="cf99a-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="cf99a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf99a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf99a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cf99a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="cf99a-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="cf99a-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="cf99a-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf99a-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="cf99a-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="cf99a-128">-SyncGroupName</span></span>
<span data-ttu-id="cf99a-129">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf99a-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="cf99a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf99a-130">CommonParameters</span></span>
<span data-ttu-id="cf99a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf99a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf99a-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf99a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf99a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cf99a-133">INPUTS</span></span>

### <span data-ttu-id="cf99a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cf99a-134">System.String</span></span>

### <span data-ttu-id="cf99a-135">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="cf99a-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="cf99a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cf99a-136">OUTPUTS</span></span>

### <span data-ttu-id="cf99a-137">PSCloudEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="cf99a-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="cf99a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cf99a-138">NOTES</span></span>

## <span data-ttu-id="cf99a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf99a-139">RELATED LINKS</span></span>