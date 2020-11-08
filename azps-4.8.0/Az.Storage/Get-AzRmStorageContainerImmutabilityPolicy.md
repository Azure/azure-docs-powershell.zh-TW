---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971631"
---
# <span data-ttu-id="0a2b3-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="0a2b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2b3-103">取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="0a2b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a2b3-104">SYNTAX</span></span>

### <span data-ttu-id="0a2b3-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="0a2b3-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2b3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0a2b3-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a2b3-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="0a2b3-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a2b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="0a2b3-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2b3-109">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會取得存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="0a2b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a2b3-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2b3-111">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="0a2b3-112">這個命令會使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0a2b3-113">範例2：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="0a2b3-114">這個命令會取得含有儲存帳戶物件和容器名稱的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="0a2b3-115">範例3：使用儲存容器物件取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b3-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="0a2b3-116">這個命令會取得含儲存容器物件之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="0a2b3-117">參數</span><span class="sxs-lookup"><span data-stu-id="0a2b3-117">PARAMETERS</span></span>

### <span data-ttu-id="0a2b3-118">-容器</span><span class="sxs-lookup"><span data-stu-id="0a2b3-118">-Container</span></span>
<span data-ttu-id="0a2b3-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="0a2b3-119">Storage container object</span></span>

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

### <span data-ttu-id="0a2b3-120">-容器</span><span class="sxs-lookup"><span data-stu-id="0a2b3-120">-ContainerName</span></span>
<span data-ttu-id="0a2b3-121">容器名稱</span><span class="sxs-lookup"><span data-stu-id="0a2b3-121">Container Name</span></span>

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

### <span data-ttu-id="0a2b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2b3-122">-DefaultProfile</span></span>
<span data-ttu-id="0a2b3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a2b3-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="0a2b3-124">-Etag</span></span>
<span data-ttu-id="0a2b3-125">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="0a2b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a2b3-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a2b3-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a2b3-128">-StorageAccount</span></span>
<span data-ttu-id="0a2b3-129">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="0a2b3-129">Storage account object</span></span>

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

### <span data-ttu-id="0a2b3-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0a2b3-130">-StorageAccountName</span></span>
<span data-ttu-id="0a2b3-131">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="0a2b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2b3-132">CommonParameters</span></span>
<span data-ttu-id="0a2b3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2b3-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2b3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0a2b3-135">INPUTS</span></span>

### <span data-ttu-id="0a2b3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="0a2b3-136">System.String</span></span>

### <span data-ttu-id="0a2b3-137">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0a2b3-138">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0a2b3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0a2b3-139">OUTPUTS</span></span>

### <span data-ttu-id="0a2b3-140">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0a2b3-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0a2b3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0a2b3-141">NOTES</span></span>

## <span data-ttu-id="0a2b3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a2b3-142">RELATED LINKS</span></span>
