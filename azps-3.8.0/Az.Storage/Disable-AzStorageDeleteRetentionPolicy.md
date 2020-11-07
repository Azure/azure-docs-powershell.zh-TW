---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957198"
---
# <span data-ttu-id="d9bed-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9bed-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d9bed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9bed-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bed-103">停用 Azure Storage Blob 服務的 [刪除保留原則]。</span><span class="sxs-lookup"><span data-stu-id="d9bed-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d9bed-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9bed-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bed-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9bed-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bed-106">**Disable AzStorageDeleteRetentionPolicy** Cmdlet 會停用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="d9bed-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d9bed-107">示例</span><span class="sxs-lookup"><span data-stu-id="d9bed-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bed-108">範例1：停用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="d9bed-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="d9bed-109">這個命令會停用 [刪除 Blob 服務的保留原則]。</span><span class="sxs-lookup"><span data-stu-id="d9bed-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="d9bed-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9bed-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bed-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d9bed-111">-Context</span></span>
<span data-ttu-id="d9bed-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="d9bed-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d9bed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bed-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bed-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9bed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bed-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9bed-115">-PassThru</span></span>
<span data-ttu-id="d9bed-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="d9bed-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="d9bed-117">-確認</span><span class="sxs-lookup"><span data-stu-id="d9bed-117">-Confirm</span></span>
<span data-ttu-id="d9bed-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9bed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bed-119">-WhatIf</span></span>
<span data-ttu-id="d9bed-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9bed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bed-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9bed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bed-122">CommonParameters</span></span>
<span data-ttu-id="d9bed-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9bed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bed-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9bed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bed-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d9bed-125">INPUTS</span></span>

### <span data-ttu-id="d9bed-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="d9bed-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d9bed-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d9bed-127">OUTPUTS</span></span>

### <span data-ttu-id="d9bed-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9bed-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d9bed-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d9bed-129">NOTES</span></span>

## <span data-ttu-id="d9bed-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9bed-130">RELATED LINKS</span></span>
