---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 81baab4f996d7a56b64f055f94a18c09b4305991
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907209"
---
# <span data-ttu-id="87923-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87923-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="87923-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87923-102">SYNOPSIS</span></span>
<span data-ttu-id="87923-103">此命令會列出特定同步處理群組內的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="87923-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="87923-104">語法</span><span class="sxs-lookup"><span data-stu-id="87923-104">SYNTAX</span></span>

### <span data-ttu-id="87923-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87923-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87923-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87923-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87923-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="87923-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87923-108">描述</span><span class="sxs-lookup"><span data-stu-id="87923-108">DESCRIPTION</span></span>
<span data-ttu-id="87923-109">此命令會列出特定同步處理群組內的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="87923-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="87923-110">它可以用來列出每個伺服器端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="87923-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="87923-111">例子</span><span class="sxs-lookup"><span data-stu-id="87923-111">EXAMPLES</span></span>

### <span data-ttu-id="87923-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="87923-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="87923-113">此命令會獲得指定同步處理群組中包含的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="87923-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="87923-114">指定 -ServerEndpointName 以返回特定名稱。</span><span class="sxs-lookup"><span data-stu-id="87923-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="87923-115">參數</span><span class="sxs-lookup"><span data-stu-id="87923-115">PARAMETERS</span></span>

### <span data-ttu-id="87923-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87923-116">-DefaultProfile</span></span>
<span data-ttu-id="87923-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87923-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87923-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="87923-118">-Name</span></span>
<span data-ttu-id="87923-119">伺服器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="87923-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87923-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="87923-120">-ParentObject</span></span>
<span data-ttu-id="87923-121">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="87923-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="87923-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="87923-122">-ParentResourceId</span></span>
<span data-ttu-id="87923-123">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="87923-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="87923-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87923-124">-ResourceGroupName</span></span>
<span data-ttu-id="87923-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="87923-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="87923-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="87923-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="87923-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="87923-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="87923-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="87923-128">-SyncGroupName</span></span>
<span data-ttu-id="87923-129">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87923-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="87923-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87923-130">CommonParameters</span></span>
<span data-ttu-id="87923-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87923-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87923-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="87923-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87923-133">輸入</span><span class="sxs-lookup"><span data-stu-id="87923-133">INPUTS</span></span>

### <span data-ttu-id="87923-134">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="87923-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="87923-135">System.String</span><span class="sxs-lookup"><span data-stu-id="87923-135">System.String</span></span>

## <span data-ttu-id="87923-136">輸出</span><span class="sxs-lookup"><span data-stu-id="87923-136">OUTPUTS</span></span>

### <span data-ttu-id="87923-137">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87923-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="87923-138">筆記</span><span class="sxs-lookup"><span data-stu-id="87923-138">NOTES</span></span>

## <span data-ttu-id="87923-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="87923-139">RELATED LINKS</span></span>
