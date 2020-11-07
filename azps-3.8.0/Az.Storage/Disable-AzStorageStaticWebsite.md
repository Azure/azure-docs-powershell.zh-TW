---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957195"
---
# <span data-ttu-id="c2bb9-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c2bb9-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="c2bb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bb9-103">停用 Azure 儲存空間帳戶的靜態網站。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c2bb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2bb9-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2bb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="c2bb9-106">**Disable AzStorageStaticWebsite** Cmdlet 會針對 Azure 儲存空間帳戶停用靜態網站。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c2bb9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="c2bb9-108">範例1：停用 Azure 儲存空間帳戶的靜態網站</span><span class="sxs-lookup"><span data-stu-id="c2bb9-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="c2bb9-109">這個命令會針對 Azure 儲存空間帳戶停用靜態網站。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="c2bb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2bb9-110">PARAMETERS</span></span>

### <span data-ttu-id="c2bb9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c2bb9-111">-Context</span></span>
<span data-ttu-id="c2bb9-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="c2bb9-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c2bb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bb9-113">-DefaultProfile</span></span>
<span data-ttu-id="c2bb9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2bb9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2bb9-115">-PassThru</span></span>
<span data-ttu-id="c2bb9-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c2bb9-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2bb9-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c2bb9-117">-Confirm</span></span>
<span data-ttu-id="c2bb9-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2bb9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2bb9-119">-WhatIf</span></span>
<span data-ttu-id="c2bb9-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2bb9-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2bb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bb9-122">CommonParameters</span></span>
<span data-ttu-id="c2bb9-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bb9-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2bb9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bb9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c2bb9-125">INPUTS</span></span>

### <span data-ttu-id="c2bb9-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c2bb9-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2bb9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c2bb9-127">OUTPUTS</span></span>

### <span data-ttu-id="c2bb9-128">WindowsAzure. ResourceModel.. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="c2bb9-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="c2bb9-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c2bb9-129">NOTES</span></span>

## <span data-ttu-id="c2bb9-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2bb9-130">RELATED LINKS</span></span>
