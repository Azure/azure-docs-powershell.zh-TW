---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611841"
---
# <span data-ttu-id="b246c-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="b246c-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="b246c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b246c-102">SYNOPSIS</span></span>
<span data-ttu-id="b246c-103">為媒體服務 Cmdlet 建立儲存帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="b246c-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="b246c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b246c-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b246c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b246c-105">DESCRIPTION</span></span>
<span data-ttu-id="b246c-106">**新的 AzMediaServiceStorageConfig** Cmdlet 會建立媒體服務 Cmdlet 的儲存帳戶配置。</span><span class="sxs-lookup"><span data-stu-id="b246c-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="b246c-107">示例</span><span class="sxs-lookup"><span data-stu-id="b246c-107">EXAMPLES</span></span>

### <span data-ttu-id="b246c-108">範例1：建立媒體服務 Cmdlet 的儲存帳戶設定</span><span class="sxs-lookup"><span data-stu-id="b246c-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="b246c-109">第一個命令會使用 **AzStorageAccount** Cmdlet 建立儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="b246c-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="b246c-110">命令會將此儲存帳戶 Storage1 及類型命名為 Standard_GRS，並將結果儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b246c-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="b246c-111">第二個命令會使用儲存在 $StorageAccount 變數中的儲存空間帳戶識別碼資訊，來建立儲存設定物件，作為與媒體服務相關聯的主要儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b246c-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="b246c-112">參數</span><span class="sxs-lookup"><span data-stu-id="b246c-112">PARAMETERS</span></span>

### <span data-ttu-id="b246c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b246c-113">-DefaultProfile</span></span>
<span data-ttu-id="b246c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b246c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b246c-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="b246c-115">-IsPrimary</span></span>
<span data-ttu-id="b246c-116">表示 Cmdlet 會建立儲存空間帳戶做為媒體服務的主要儲存空間。</span><span class="sxs-lookup"><span data-stu-id="b246c-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b246c-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b246c-117">-StorageAccountId</span></span>
<span data-ttu-id="b246c-118">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="b246c-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="b246c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b246c-119">-Confirm</span></span>
<span data-ttu-id="b246c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b246c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b246c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b246c-121">-WhatIf</span></span>
<span data-ttu-id="b246c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b246c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b246c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b246c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b246c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b246c-124">CommonParameters</span></span>
<span data-ttu-id="b246c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b246c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b246c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b246c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b246c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b246c-127">INPUTS</span></span>

### <span data-ttu-id="b246c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b246c-128">System.String</span></span>

## <span data-ttu-id="b246c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b246c-129">OUTPUTS</span></span>

### <span data-ttu-id="b246c-130">PSStorageAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b246c-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b246c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b246c-131">NOTES</span></span>

## <span data-ttu-id="b246c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b246c-132">RELATED LINKS</span></span>

[<span data-ttu-id="b246c-133">同步處理-AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="b246c-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)


