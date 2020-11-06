---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454471"
---
# <span data-ttu-id="2e6f6-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="2e6f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6f6-103">取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e6f6-104">SYNTAX</span></span>

### <span data-ttu-id="2e6f6-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="2e6f6-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6f6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2e6f6-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6f6-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2e6f6-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e6f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="2e6f6-108">DESCRIPTION</span></span>
<span data-ttu-id="2e6f6-109">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet 會取得存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="2e6f6-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e6f6-110">EXAMPLES</span></span>

### <span data-ttu-id="2e6f6-111">範例1：使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="2e6f6-112">這個命令會使用儲存空間帳戶名稱和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="2e6f6-113">範例2：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="2e6f6-114">這個命令會取得含有儲存帳戶物件和容器名稱的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="2e6f6-115">範例3：使用儲存容器物件取得儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f6-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="2e6f6-116">這個命令會取得含儲存容器物件之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="2e6f6-117">參數</span><span class="sxs-lookup"><span data-stu-id="2e6f6-117">PARAMETERS</span></span>

### <span data-ttu-id="2e6f6-118">-容器</span><span class="sxs-lookup"><span data-stu-id="2e6f6-118">-Container</span></span>
<span data-ttu-id="2e6f6-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="2e6f6-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-120">-容器</span><span class="sxs-lookup"><span data-stu-id="2e6f6-120">-ContainerName</span></span>
<span data-ttu-id="2e6f6-121">容器名稱</span><span class="sxs-lookup"><span data-stu-id="2e6f6-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6f6-122">-DefaultProfile</span></span>
<span data-ttu-id="2e6f6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="2e6f6-124">-Etag</span></span>
<span data-ttu-id="2e6f6-125">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6f6-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e6f6-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e6f6-128">-StorageAccount</span></span>
<span data-ttu-id="2e6f6-129">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2e6f6-129">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2e6f6-130">-StorageAccountName</span></span>
<span data-ttu-id="2e6f6-131">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-131">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6f6-132">CommonParameters</span></span>
<span data-ttu-id="2e6f6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6f6-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6f6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2e6f6-135">INPUTS</span></span>

### <span data-ttu-id="2e6f6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="2e6f6-136">System.String</span></span>

## <span data-ttu-id="2e6f6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2e6f6-137">OUTPUTS</span></span>

### <span data-ttu-id="2e6f6-138">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2e6f6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="2e6f6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2e6f6-139">NOTES</span></span>

## <span data-ttu-id="2e6f6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e6f6-140">RELATED LINKS</span></span>

