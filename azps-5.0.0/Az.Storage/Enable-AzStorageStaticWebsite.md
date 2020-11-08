---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137465"
---
# <span data-ttu-id="ebd28-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ebd28-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="ebd28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebd28-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd28-103">針對 Azure 儲存空間帳戶啟用靜態網站。</span><span class="sxs-lookup"><span data-stu-id="ebd28-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ebd28-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebd28-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebd28-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebd28-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd28-106">**Enable-AzStorageStaticWebsite** Cmdlet 可為 Azure 儲存空間帳戶啟用靜態網站。</span><span class="sxs-lookup"><span data-stu-id="ebd28-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ebd28-107">示例</span><span class="sxs-lookup"><span data-stu-id="ebd28-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd28-108">範例1：針對 Azure 儲存空間帳戶啟用靜態網站</span><span class="sxs-lookup"><span data-stu-id="ebd28-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="ebd28-109">此命令會針對 Azure 儲存空間帳戶啟用靜態網站。</span><span class="sxs-lookup"><span data-stu-id="ebd28-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="ebd28-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebd28-110">PARAMETERS</span></span>

### <span data-ttu-id="ebd28-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ebd28-111">-Context</span></span>
<span data-ttu-id="ebd28-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="ebd28-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ebd28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd28-113">-DefaultProfile</span></span>
<span data-ttu-id="ebd28-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebd28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd28-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="ebd28-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="ebd28-116">發佈404時，應顯示的錯誤檔路徑 (意味著瀏覽器要求不存在的頁面。 ) </span><span class="sxs-lookup"><span data-stu-id="ebd28-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd28-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="ebd28-117">-IndexDocument</span></span>
<span data-ttu-id="ebd28-118">每個目錄中的索引檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="ebd28-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd28-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebd28-119">-PassThru</span></span>
<span data-ttu-id="ebd28-120">[在 ServiceProperties 中顯示靜態網站] 設定。</span><span class="sxs-lookup"><span data-stu-id="ebd28-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="ebd28-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ebd28-121">-Confirm</span></span>
<span data-ttu-id="ebd28-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebd28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebd28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebd28-123">-WhatIf</span></span>
<span data-ttu-id="ebd28-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebd28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebd28-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebd28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebd28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd28-126">CommonParameters</span></span>
<span data-ttu-id="ebd28-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebd28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd28-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebd28-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd28-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ebd28-129">INPUTS</span></span>

### <span data-ttu-id="ebd28-130">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ebd28-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ebd28-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ebd28-131">OUTPUTS</span></span>

### <span data-ttu-id="ebd28-132">WindowsAzure. ResourceModel.. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="ebd28-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="ebd28-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ebd28-133">NOTES</span></span>

## <span data-ttu-id="ebd28-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebd28-134">RELATED LINKS</span></span>
