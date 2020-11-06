---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2b324d1b038a6ab97e4e68303bd98570fe0704ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614629"
---
# <span data-ttu-id="d8ce9-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d8ce9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ce9-103">取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d8ce9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8ce9-104">SYNTAX</span></span>

### <span data-ttu-id="d8ce9-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="d8ce9-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ce9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d8ce9-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ce9-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d8ce9-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8ce9-108">說明</span><span class="sxs-lookup"><span data-stu-id="d8ce9-108">DESCRIPTION</span></span>
<span data-ttu-id="d8ce9-109">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會取得存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d8ce9-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8ce9-110">EXAMPLES</span></span>

### <span data-ttu-id="d8ce9-111">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="d8ce9-112">這個命令會使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d8ce9-113">範例2：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="d8ce9-114">這個命令會取得含有儲存帳戶物件和容器名稱的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="d8ce9-115">範例3：使用儲存容器物件取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ce9-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="d8ce9-116">這個命令會取得含儲存容器物件之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="d8ce9-117">參數</span><span class="sxs-lookup"><span data-stu-id="d8ce9-117">PARAMETERS</span></span>

### <span data-ttu-id="d8ce9-118">-容器</span><span class="sxs-lookup"><span data-stu-id="d8ce9-118">-Container</span></span>
<span data-ttu-id="d8ce9-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="d8ce9-119">Storage container object</span></span>

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

### <span data-ttu-id="d8ce9-120">-容器</span><span class="sxs-lookup"><span data-stu-id="d8ce9-120">-ContainerName</span></span>
<span data-ttu-id="d8ce9-121">容器名稱</span><span class="sxs-lookup"><span data-stu-id="d8ce9-121">Container Name</span></span>

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

### <span data-ttu-id="d8ce9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ce9-122">-DefaultProfile</span></span>
<span data-ttu-id="d8ce9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ce9-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="d8ce9-124">-Etag</span></span>
<span data-ttu-id="d8ce9-125">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="d8ce9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ce9-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8ce9-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d8ce9-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8ce9-128">-StorageAccount</span></span>
<span data-ttu-id="d8ce9-129">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d8ce9-129">Storage account object</span></span>

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

### <span data-ttu-id="d8ce9-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8ce9-130">-StorageAccountName</span></span>
<span data-ttu-id="d8ce9-131">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="d8ce9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ce9-132">CommonParameters</span></span>
<span data-ttu-id="d8ce9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ce9-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ce9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d8ce9-135">INPUTS</span></span>

### <span data-ttu-id="d8ce9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d8ce9-136">System.String</span></span>

### <span data-ttu-id="d8ce9-137">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d8ce9-138">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d8ce9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d8ce9-139">OUTPUTS</span></span>

### <span data-ttu-id="d8ce9-140">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d8ce9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d8ce9-141">NOTES</span></span>

## <span data-ttu-id="d8ce9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8ce9-142">RELATED LINKS</span></span>
