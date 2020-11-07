---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801109"
---
# <span data-ttu-id="77c88-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="77c88-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="77c88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77c88-102">SYNOPSIS</span></span>
<span data-ttu-id="77c88-103">停用 Azure Storage Blob 服務的 [刪除保留原則]。</span><span class="sxs-lookup"><span data-stu-id="77c88-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77c88-104">句法</span><span class="sxs-lookup"><span data-stu-id="77c88-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c88-105">說明</span><span class="sxs-lookup"><span data-stu-id="77c88-105">DESCRIPTION</span></span>
<span data-ttu-id="77c88-106">**Disable AzureStorageDeleteRetentionPolicy** Cmdlet 會停用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="77c88-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="77c88-107">示例</span><span class="sxs-lookup"><span data-stu-id="77c88-107">EXAMPLES</span></span>

### <span data-ttu-id="77c88-108">範例1：停用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="77c88-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="77c88-109">這個命令會停用 [刪除 Blob 服務的保留原則]。</span><span class="sxs-lookup"><span data-stu-id="77c88-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="77c88-110">參數</span><span class="sxs-lookup"><span data-stu-id="77c88-110">PARAMETERS</span></span>

### <span data-ttu-id="77c88-111">-內容</span><span class="sxs-lookup"><span data-stu-id="77c88-111">-Context</span></span>
<span data-ttu-id="77c88-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="77c88-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="77c88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c88-113">-DefaultProfile</span></span>
<span data-ttu-id="77c88-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77c88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c88-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77c88-115">-PassThru</span></span>
<span data-ttu-id="77c88-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="77c88-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="77c88-117">-確認</span><span class="sxs-lookup"><span data-stu-id="77c88-117">-Confirm</span></span>
<span data-ttu-id="77c88-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77c88-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c88-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c88-119">-WhatIf</span></span>
<span data-ttu-id="77c88-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77c88-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77c88-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77c88-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c88-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c88-122">CommonParameters</span></span>
<span data-ttu-id="77c88-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77c88-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c88-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77c88-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c88-125">輸入</span><span class="sxs-lookup"><span data-stu-id="77c88-125">INPUTS</span></span>

### <span data-ttu-id="77c88-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="77c88-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="77c88-127">輸出</span><span class="sxs-lookup"><span data-stu-id="77c88-127">OUTPUTS</span></span>

### <span data-ttu-id="77c88-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="77c88-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="77c88-129">筆記</span><span class="sxs-lookup"><span data-stu-id="77c88-129">NOTES</span></span>

## <span data-ttu-id="77c88-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="77c88-130">RELATED LINKS</span></span>
