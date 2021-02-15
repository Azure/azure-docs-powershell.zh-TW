---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136079"
---
# <span data-ttu-id="901be-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="901be-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="901be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="901be-102">SYNOPSIS</span></span>
<span data-ttu-id="901be-103">針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="901be-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="901be-104">句法</span><span class="sxs-lookup"><span data-stu-id="901be-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="901be-105">說明</span><span class="sxs-lookup"><span data-stu-id="901be-105">DESCRIPTION</span></span>
<span data-ttu-id="901be-106">**Sync-AzMediaServiceStorageKey** Cmdlet 會針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="901be-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="901be-107">示例</span><span class="sxs-lookup"><span data-stu-id="901be-107">EXAMPLES</span></span>

### <span data-ttu-id="901be-108">範例1：針對與媒體服務相關聯的儲存空間帳戶同步處理儲存空間帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="901be-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="901be-109">第一個命令使用 Get-AzStorageAccount Cmdlet 來取得名為 Storage135 的 ResourceGroup001 儲存帳戶，並將結果儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="901be-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="901be-110">第二個命令會使用 $StorageAccount 變數中包含的 **Id** 屬性，同步處理名為 MediaService001 的媒體服務的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="901be-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="901be-111">參數</span><span class="sxs-lookup"><span data-stu-id="901be-111">PARAMETERS</span></span>

### <span data-ttu-id="901be-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="901be-112">-AccountName</span></span>
<span data-ttu-id="901be-113">指定此 Cmdlet 同步處理的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="901be-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="901be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901be-114">-DefaultProfile</span></span>
<span data-ttu-id="901be-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="901be-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="901be-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901be-116">-ResourceGroupName</span></span>
<span data-ttu-id="901be-117">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="901be-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="901be-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="901be-118">-StorageAccountId</span></span>
<span data-ttu-id="901be-119">指定與媒體服務帳戶相關聯的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="901be-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="901be-120">-確認</span><span class="sxs-lookup"><span data-stu-id="901be-120">-Confirm</span></span>
<span data-ttu-id="901be-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="901be-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="901be-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901be-122">-WhatIf</span></span>
<span data-ttu-id="901be-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="901be-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="901be-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="901be-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="901be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901be-125">CommonParameters</span></span>
<span data-ttu-id="901be-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="901be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901be-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="901be-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901be-128">輸入</span><span class="sxs-lookup"><span data-stu-id="901be-128">INPUTS</span></span>

### <span data-ttu-id="901be-129">System.object</span><span class="sxs-lookup"><span data-stu-id="901be-129">System.String</span></span>

## <span data-ttu-id="901be-130">輸出</span><span class="sxs-lookup"><span data-stu-id="901be-130">OUTPUTS</span></span>

### <span data-ttu-id="901be-131">System.object</span><span class="sxs-lookup"><span data-stu-id="901be-131">System.Boolean</span></span>

## <span data-ttu-id="901be-132">筆記</span><span class="sxs-lookup"><span data-stu-id="901be-132">NOTES</span></span>

## <span data-ttu-id="901be-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="901be-133">RELATED LINKS</span></span>
