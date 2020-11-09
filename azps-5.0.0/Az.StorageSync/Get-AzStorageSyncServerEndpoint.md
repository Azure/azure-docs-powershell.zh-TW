---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287663"
---
# <span data-ttu-id="f8fb6-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fb6-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="f8fb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fb6-103">這個命令會列出指定同步群組中的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="f8fb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8fb6-104">SYNTAX</span></span>

### <span data-ttu-id="f8fb6-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f8fb6-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8fb6-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8fb6-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8fb6-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8fb6-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fb6-108">說明</span><span class="sxs-lookup"><span data-stu-id="f8fb6-108">DESCRIPTION</span></span>
<span data-ttu-id="f8fb6-109">這個命令會列出指定同步群組中的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="f8fb6-110">您也可以使用它來列出每個伺服器端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="f8fb6-111">示例</span><span class="sxs-lookup"><span data-stu-id="f8fb6-111">EXAMPLES</span></span>

### <span data-ttu-id="f8fb6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f8fb6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="f8fb6-113">這個命令會取得指定同步群組中所包含的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="f8fb6-114">指定-ServerEndpointName 以傳回特定的專案。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="f8fb6-115">參數</span><span class="sxs-lookup"><span data-stu-id="f8fb6-115">PARAMETERS</span></span>

### <span data-ttu-id="f8fb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fb6-116">-DefaultProfile</span></span>
<span data-ttu-id="f8fb6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8fb6-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8fb6-118">-Name</span></span>
<span data-ttu-id="f8fb6-119">伺服器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="f8fb6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f8fb6-120">-ParentObject</span></span>
<span data-ttu-id="f8fb6-121">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f8fb6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f8fb6-122">-ParentResourceId</span></span>
<span data-ttu-id="f8fb6-123">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f8fb6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fb6-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8fb6-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8fb6-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f8fb6-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="f8fb6-127">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f8fb6-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fb6-128">-SyncGroupName</span></span>
<span data-ttu-id="f8fb6-129">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="f8fb6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fb6-130">CommonParameters</span></span>
<span data-ttu-id="f8fb6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fb6-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fb6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f8fb6-133">INPUTS</span></span>

### <span data-ttu-id="f8fb6-134">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="f8fb6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f8fb6-135">System.String</span></span>

## <span data-ttu-id="f8fb6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f8fb6-136">OUTPUTS</span></span>

### <span data-ttu-id="f8fb6-137">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="f8fb6-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="f8fb6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f8fb6-138">NOTES</span></span>

## <span data-ttu-id="f8fb6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8fb6-139">RELATED LINKS</span></span>
