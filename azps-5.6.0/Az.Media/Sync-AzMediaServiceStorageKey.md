---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 75e83c3d861bfbe579634da0ee136f564be43ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909666"
---
# <span data-ttu-id="03d7c-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="03d7c-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="03d7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="03d7c-103">同步處理與媒體服務相關聯的儲存空間帳戶的儲存帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="03d7c-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="03d7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="03d7c-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03d7c-105">描述</span><span class="sxs-lookup"><span data-stu-id="03d7c-105">DESCRIPTION</span></span>
<span data-ttu-id="03d7c-106">**Sync-AzMediaServiceStorageKey Cmdlet** 會同步處理與媒體服務相關聯的儲存空間帳戶的儲存帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="03d7c-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="03d7c-107">例子</span><span class="sxs-lookup"><span data-stu-id="03d7c-107">EXAMPLES</span></span>

### <span data-ttu-id="03d7c-108">範例 1：同步處理與媒體服務相關聯的儲存空間帳戶的儲存帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="03d7c-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="03d7c-109">第一個命令使用 Get-AzStorageAccount Cmdlet 取得名稱為 Storage135 的儲存帳戶，該帳戶屬於 ResourceGroup001，並且將結果儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="03d7c-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="03d7c-110">第二個命令會使用 $StorageAccount 變數中包含的 **Id** 屬性，同步媒體服務名為 MediaService001 的儲存$StorageAccount金鑰。</span><span class="sxs-lookup"><span data-stu-id="03d7c-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="03d7c-111">參數</span><span class="sxs-lookup"><span data-stu-id="03d7c-111">PARAMETERS</span></span>

### <span data-ttu-id="03d7c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03d7c-112">-AccountName</span></span>
<span data-ttu-id="03d7c-113">指定此 Cmdlet 同步的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="03d7c-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d7c-114">-DefaultProfile</span></span>
<span data-ttu-id="03d7c-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="03d7c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03d7c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03d7c-116">-ResourceGroupName</span></span>
<span data-ttu-id="03d7c-117">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="03d7c-117">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d7c-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="03d7c-118">-StorageAccountId</span></span>
<span data-ttu-id="03d7c-119">指定與媒體服務帳戶相關聯的儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="03d7c-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d7c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="03d7c-120">-Confirm</span></span>
<span data-ttu-id="03d7c-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03d7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03d7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d7c-122">-WhatIf</span></span>
<span data-ttu-id="03d7c-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03d7c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03d7c-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03d7c-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03d7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d7c-125">CommonParameters</span></span>
<span data-ttu-id="03d7c-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03d7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d7c-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="03d7c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d7c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="03d7c-128">INPUTS</span></span>

### <span data-ttu-id="03d7c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="03d7c-129">System.String</span></span>

## <span data-ttu-id="03d7c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="03d7c-130">OUTPUTS</span></span>

### <span data-ttu-id="03d7c-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03d7c-131">System.Boolean</span></span>

## <span data-ttu-id="03d7c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="03d7c-132">NOTES</span></span>

## <span data-ttu-id="03d7c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="03d7c-133">RELATED LINKS</span></span>
