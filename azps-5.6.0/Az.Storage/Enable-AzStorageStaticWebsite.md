---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: 25526e7c83746b67a5272ab94f3d523947795c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907250"
---
# <span data-ttu-id="525cf-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="525cf-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="525cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="525cf-102">SYNOPSIS</span></span>
<span data-ttu-id="525cf-103">啟用 Azure 儲存空間帳戶的靜態網站。</span><span class="sxs-lookup"><span data-stu-id="525cf-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="525cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="525cf-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="525cf-105">描述</span><span class="sxs-lookup"><span data-stu-id="525cf-105">DESCRIPTION</span></span>
<span data-ttu-id="525cf-106">**Enable-AzStorageStaticWebsite** Cmdlet 可啟用 Azure 儲存體帳戶的靜態網站。</span><span class="sxs-lookup"><span data-stu-id="525cf-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="525cf-107">例子</span><span class="sxs-lookup"><span data-stu-id="525cf-107">EXAMPLES</span></span>

### <span data-ttu-id="525cf-108">範例 1：啟用 Azure 儲存體帳戶的靜態網站</span><span class="sxs-lookup"><span data-stu-id="525cf-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="525cf-109">此命令會啟用 Azure 儲存體帳戶的靜態網站。</span><span class="sxs-lookup"><span data-stu-id="525cf-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="525cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="525cf-110">PARAMETERS</span></span>

### <span data-ttu-id="525cf-111">-內容</span><span class="sxs-lookup"><span data-stu-id="525cf-111">-Context</span></span>
<span data-ttu-id="525cf-112">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="525cf-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="525cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525cf-113">-DefaultProfile</span></span>
<span data-ttu-id="525cf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="525cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525cf-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="525cf-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="525cf-116">當瀏覽器要求不存在的頁面時，當 404 發行時 (錯誤檔的路徑。) </span><span class="sxs-lookup"><span data-stu-id="525cf-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="525cf-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="525cf-117">-IndexDocument</span></span>
<span data-ttu-id="525cf-118">索引檔在每個目錄中的名稱。</span><span class="sxs-lookup"><span data-stu-id="525cf-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="525cf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="525cf-119">-PassThru</span></span>
<span data-ttu-id="525cf-120">在 ServiceProperties 中顯示靜態網站設定。</span><span class="sxs-lookup"><span data-stu-id="525cf-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="525cf-121">-確認</span><span class="sxs-lookup"><span data-stu-id="525cf-121">-Confirm</span></span>
<span data-ttu-id="525cf-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="525cf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525cf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525cf-123">-WhatIf</span></span>
<span data-ttu-id="525cf-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="525cf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="525cf-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="525cf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525cf-126">CommonParameters</span></span>
<span data-ttu-id="525cf-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="525cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525cf-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="525cf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525cf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="525cf-129">INPUTS</span></span>

### <span data-ttu-id="525cf-130">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="525cf-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="525cf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="525cf-131">OUTPUTS</span></span>

### <span data-ttu-id="525cf-132">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="525cf-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="525cf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="525cf-133">NOTES</span></span>

## <span data-ttu-id="525cf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="525cf-134">RELATED LINKS</span></span>
