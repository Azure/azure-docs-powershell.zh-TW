---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 1d55c52b3c022e9e935051cdb1ad23aae32eecbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907261"
---
# <span data-ttu-id="aeb59-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb59-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="aeb59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aeb59-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb59-103">啟用 Azure 儲存體 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="aeb59-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="aeb59-104">語法</span><span class="sxs-lookup"><span data-stu-id="aeb59-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb59-105">描述</span><span class="sxs-lookup"><span data-stu-id="aeb59-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb59-106">**Enable-AzStorageDeleteRetentionPolicy** Cmdlet 可啟用 Azure 儲存體 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="aeb59-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="aeb59-107">例子</span><span class="sxs-lookup"><span data-stu-id="aeb59-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb59-108">範例 1：啟用 Blob 服務的刪除保留原則</span><span class="sxs-lookup"><span data-stu-id="aeb59-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="aeb59-109">此命令會啟用 Blob 服務的刪除保留原則，並且將已刪除的 Blob 保留天數設為 3。</span><span class="sxs-lookup"><span data-stu-id="aeb59-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="aeb59-110">參數</span><span class="sxs-lookup"><span data-stu-id="aeb59-110">PARAMETERS</span></span>

### <span data-ttu-id="aeb59-111">-內容</span><span class="sxs-lookup"><span data-stu-id="aeb59-111">-Context</span></span>
<span data-ttu-id="aeb59-112">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="aeb59-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="aeb59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb59-113">-DefaultProfile</span></span>
<span data-ttu-id="aeb59-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aeb59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb59-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aeb59-115">-PassThru</span></span>
<span data-ttu-id="aeb59-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="aeb59-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="aeb59-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="aeb59-117">-RetentionDays</span></span>
<span data-ttu-id="aeb59-118">設定 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="aeb59-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="aeb59-119">-確認</span><span class="sxs-lookup"><span data-stu-id="aeb59-119">-Confirm</span></span>
<span data-ttu-id="aeb59-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aeb59-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb59-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb59-121">-WhatIf</span></span>
<span data-ttu-id="aeb59-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aeb59-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeb59-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aeb59-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb59-124">CommonParameters</span></span>
<span data-ttu-id="aeb59-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aeb59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb59-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="aeb59-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb59-127">輸入</span><span class="sxs-lookup"><span data-stu-id="aeb59-127">INPUTS</span></span>

### <span data-ttu-id="aeb59-128">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="aeb59-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aeb59-129">輸出</span><span class="sxs-lookup"><span data-stu-id="aeb59-129">OUTPUTS</span></span>

### <span data-ttu-id="aeb59-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aeb59-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="aeb59-131">筆記</span><span class="sxs-lookup"><span data-stu-id="aeb59-131">NOTES</span></span>

## <span data-ttu-id="aeb59-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="aeb59-132">RELATED LINKS</span></span>
