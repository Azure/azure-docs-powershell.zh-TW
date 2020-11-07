---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f09ba3cdd0404f1eca21540a6893f1bcd67f05e5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795170"
---
# <span data-ttu-id="4f78f-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f78f-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="4f78f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f78f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f78f-103">停用 Azure Storage Blob 服務的 [刪除保留原則]。</span><span class="sxs-lookup"><span data-stu-id="4f78f-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="4f78f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f78f-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f78f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f78f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f78f-106">**Disable AzStorageDeleteRetentionPolicy** Cmdlet 會停用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="4f78f-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="4f78f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f78f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f78f-108">範例1：停用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="4f78f-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="4f78f-109">這個命令會停用 [刪除 Blob 服務的保留原則]。</span><span class="sxs-lookup"><span data-stu-id="4f78f-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="4f78f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f78f-110">PARAMETERS</span></span>

### <span data-ttu-id="4f78f-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4f78f-111">-Context</span></span>
<span data-ttu-id="4f78f-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="4f78f-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4f78f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f78f-113">-DefaultProfile</span></span>
<span data-ttu-id="4f78f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f78f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f78f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f78f-115">-PassThru</span></span>
<span data-ttu-id="4f78f-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4f78f-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="4f78f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="4f78f-117">-Confirm</span></span>
<span data-ttu-id="4f78f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f78f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f78f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f78f-119">-WhatIf</span></span>
<span data-ttu-id="4f78f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f78f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f78f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f78f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f78f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f78f-122">CommonParameters</span></span>
<span data-ttu-id="4f78f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f78f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f78f-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f78f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f78f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4f78f-125">INPUTS</span></span>

### <span data-ttu-id="4f78f-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="4f78f-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f78f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4f78f-127">OUTPUTS</span></span>

### <span data-ttu-id="4f78f-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f78f-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="4f78f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4f78f-129">NOTES</span></span>

## <span data-ttu-id="4f78f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f78f-130">RELATED LINKS</span></span>
