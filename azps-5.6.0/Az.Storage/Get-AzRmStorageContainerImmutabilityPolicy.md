---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c1e68d77df44688961f867d473a9dfce1205c2dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915170"
---
# <span data-ttu-id="a32eb-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a32eb-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a32eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a32eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a32eb-103">獲取儲存 Blob 容器的服務性</span><span class="sxs-lookup"><span data-stu-id="a32eb-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a32eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="a32eb-104">SYNTAX</span></span>

### <span data-ttu-id="a32eb-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="a32eb-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a32eb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a32eb-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a32eb-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a32eb-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a32eb-108">描述</span><span class="sxs-lookup"><span data-stu-id="a32eb-108">DESCRIPTION</span></span>
<span data-ttu-id="a32eb-109">**Get-AzRmStorageContainerImmutabilityPolidlet** 取得 Storage Blob 容器的MiutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a32eb-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a32eb-110">例子</span><span class="sxs-lookup"><span data-stu-id="a32eb-110">EXAMPLES</span></span>

### <span data-ttu-id="a32eb-111">範例 1：取得具有儲存帳戶名稱和容器名稱的儲存體 Blob 容器的 BlobPolicy</span><span class="sxs-lookup"><span data-stu-id="a32eb-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="a32eb-112">此命令會使用儲存帳戶名稱和容器名稱，來使用 Storage Blob 容器的一項指令性。</span><span class="sxs-lookup"><span data-stu-id="a32eb-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a32eb-113">範例 2：取得具有儲存帳戶物件和容器名稱的儲存體 Blob 容器的一項服務</span><span class="sxs-lookup"><span data-stu-id="a32eb-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="a32eb-114">此命令會使用儲存帳戶物件和容器名稱的儲存體 Blob 容器的一項指令性。</span><span class="sxs-lookup"><span data-stu-id="a32eb-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="a32eb-115">範例 3：取得具有儲存容器物件的儲存體 Blob 容器的一項服務</span><span class="sxs-lookup"><span data-stu-id="a32eb-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="a32eb-116">此命令會獲得包含儲存容器物件的儲存體 Blob 容器的一項指令性。</span><span class="sxs-lookup"><span data-stu-id="a32eb-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="a32eb-117">參數</span><span class="sxs-lookup"><span data-stu-id="a32eb-117">PARAMETERS</span></span>

### <span data-ttu-id="a32eb-118">-Container</span><span class="sxs-lookup"><span data-stu-id="a32eb-118">-Container</span></span>
<span data-ttu-id="a32eb-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="a32eb-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a32eb-120">-ContainerName</span></span>
<span data-ttu-id="a32eb-121">容器名稱</span><span class="sxs-lookup"><span data-stu-id="a32eb-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32eb-122">-DefaultProfile</span></span>
<span data-ttu-id="a32eb-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a32eb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a32eb-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="a32eb-124">-Etag</span></span>
<span data-ttu-id="a32eb-125">可移動性政策 etag。</span><span class="sxs-lookup"><span data-stu-id="a32eb-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a32eb-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a32eb-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a32eb-128">-StorageAccount</span></span>
<span data-ttu-id="a32eb-129">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a32eb-129">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a32eb-130">-StorageAccountName</span></span>
<span data-ttu-id="a32eb-131">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a32eb-131">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32eb-132">CommonParameters</span></span>
<span data-ttu-id="a32eb-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a32eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32eb-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a32eb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32eb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a32eb-135">INPUTS</span></span>

### <span data-ttu-id="a32eb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a32eb-136">System.String</span></span>

### <span data-ttu-id="a32eb-137">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a32eb-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a32eb-138">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a32eb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a32eb-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a32eb-139">OUTPUTS</span></span>

### <span data-ttu-id="a32eb-140">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a32eb-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a32eb-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a32eb-141">NOTES</span></span>

## <span data-ttu-id="a32eb-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a32eb-142">RELATED LINKS</span></span>
