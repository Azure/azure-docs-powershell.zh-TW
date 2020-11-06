---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 4778e0230cd50b3567cb0ded2ca629cd81db33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445867"
---
# <span data-ttu-id="b6239-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6239-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b6239-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6239-102">SYNOPSIS</span></span>
<span data-ttu-id="b6239-103">針對 Azure Storage Blob 服務啟用刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="b6239-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6239-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6239-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6239-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6239-105">DESCRIPTION</span></span>
<span data-ttu-id="b6239-106">**Enable-AzureStorageDeleteRetentionPolicy** Cmdlet 會啟用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="b6239-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b6239-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6239-107">EXAMPLES</span></span>

### <span data-ttu-id="b6239-108">範例1：啟用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="b6239-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="b6239-109">這個命令會啟用 Blob 服務的 [刪除保留原則]，並將 [刪除的 blob 保留天數] 設定為3。</span><span class="sxs-lookup"><span data-stu-id="b6239-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="b6239-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6239-110">PARAMETERS</span></span>

### <span data-ttu-id="b6239-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b6239-111">-Context</span></span>
<span data-ttu-id="b6239-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="b6239-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6239-113">-DefaultProfile</span></span>
<span data-ttu-id="b6239-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6239-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6239-115">-PassThru</span></span>
<span data-ttu-id="b6239-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b6239-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="b6239-117">-RetentionDays</span></span>
<span data-ttu-id="b6239-118">設定 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="b6239-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b6239-119">-Confirm</span></span>
<span data-ttu-id="b6239-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6239-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6239-121">-WhatIf</span></span>
<span data-ttu-id="b6239-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6239-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6239-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6239-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6239-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6239-124">CommonParameters</span></span>
<span data-ttu-id="b6239-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6239-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6239-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6239-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6239-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b6239-127">INPUTS</span></span>

### <span data-ttu-id="b6239-128">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b6239-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6239-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b6239-129">OUTPUTS</span></span>

### <span data-ttu-id="b6239-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6239-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b6239-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b6239-131">NOTES</span></span>

## <span data-ttu-id="b6239-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6239-132">RELATED LINKS</span></span>
