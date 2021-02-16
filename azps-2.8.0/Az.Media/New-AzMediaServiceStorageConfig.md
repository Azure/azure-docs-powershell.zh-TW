---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: ec411d7e1afd71849ec2d490ee70eeb0283303ca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413807"
---
# <span data-ttu-id="f0514-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="f0514-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="f0514-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0514-102">SYNOPSIS</span></span>
<span data-ttu-id="f0514-103">建立媒體服務 Cmdlet 的儲存空間帳戶組配置。</span><span class="sxs-lookup"><span data-stu-id="f0514-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="f0514-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0514-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0514-105">描述</span><span class="sxs-lookup"><span data-stu-id="f0514-105">DESCRIPTION</span></span>
<span data-ttu-id="f0514-106">**New-AzMediaServiceStorageConfig** Cmdlet 會針對媒體服務 Cmdlet 建立儲存帳戶組式。</span><span class="sxs-lookup"><span data-stu-id="f0514-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="f0514-107">例子</span><span class="sxs-lookup"><span data-stu-id="f0514-107">EXAMPLES</span></span>

### <span data-ttu-id="f0514-108">範例 1：建立媒體服務 Cmdlet 的儲存空間帳戶組</span><span class="sxs-lookup"><span data-stu-id="f0514-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="f0514-109">第一個命令會使用 **New-AzStorageAccount** Cmdlet 建立儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="f0514-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="f0514-110">命令會命名此儲存帳戶 Storage1，且類型會命名為 Standard_GRS，並儲存在名為 $StorageAccount 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f0514-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="f0514-111">第二個命令會使用儲存在資料變數中的儲存帳戶識別碼資訊，將儲存組$StorageAccount帳戶。</span><span class="sxs-lookup"><span data-stu-id="f0514-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="f0514-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0514-112">PARAMETERS</span></span>

### <span data-ttu-id="f0514-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0514-113">-DefaultProfile</span></span>
<span data-ttu-id="f0514-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f0514-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0514-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="f0514-115">-IsPrimary</span></span>
<span data-ttu-id="f0514-116">表示 Cmdlet 會建立儲存帳戶做為媒體服務的主要儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f0514-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="f0514-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f0514-117">-StorageAccountId</span></span>
<span data-ttu-id="f0514-118">指定儲存空間帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0514-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="f0514-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f0514-119">-Confirm</span></span>
<span data-ttu-id="f0514-120">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0514-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0514-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0514-121">-WhatIf</span></span>
<span data-ttu-id="f0514-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0514-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0514-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0514-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0514-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0514-124">CommonParameters</span></span>
<span data-ttu-id="f0514-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0514-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0514-126">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f0514-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0514-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f0514-127">INPUTS</span></span>

### <span data-ttu-id="f0514-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0514-128">System.String</span></span>

## <span data-ttu-id="f0514-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f0514-129">OUTPUTS</span></span>

### <span data-ttu-id="f0514-130">Microsoft.Azure.Commands.Media.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0514-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f0514-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f0514-131">NOTES</span></span>

## <span data-ttu-id="f0514-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0514-132">RELATED LINKS</span></span>



