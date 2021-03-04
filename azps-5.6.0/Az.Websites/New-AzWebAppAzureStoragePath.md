---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: b30a7736c1d3971bcdd4d7b3b776b0c439e9395b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907010"
---
# <span data-ttu-id="c4f8c-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c4f8c-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="c4f8c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c4f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f8c-103">建立代表要安裝在 Web App 中的 Azure 儲存路徑的物件。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="c4f8c-104">此參數應做為 ( AzureStoragePath) Set-AzWebAppSet-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4f8c-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c4f8c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4f8c-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f8c-106">描述</span><span class="sxs-lookup"><span data-stu-id="c4f8c-106">DESCRIPTION</span></span>
<span data-ttu-id="c4f8c-107">建立代表要安裝在 Web App 內之 Azure 儲存路徑的物件。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="c4f8c-108">例子</span><span class="sxs-lookup"><span data-stu-id="c4f8c-108">EXAMPLES</span></span>

### <span data-ttu-id="c4f8c-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="c4f8c-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="c4f8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="c4f8c-110">PARAMETERS</span></span>

### <span data-ttu-id="c4f8c-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="c4f8c-111">-AccessKey</span></span>
<span data-ttu-id="c4f8c-112">Azure 儲存空間帳戶的 Access 金鑰</span><span class="sxs-lookup"><span data-stu-id="c4f8c-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4f8c-113">-AccountName</span></span>
<span data-ttu-id="c4f8c-114">Azure 儲存體帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-114">Azure Storage account name.</span></span>
<span data-ttu-id="c4f8c-115">例如：myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c4f8c-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f8c-116">-DefaultProfile</span></span>
<span data-ttu-id="c4f8c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f8c-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="c4f8c-118">-MountPath</span></span>
<span data-ttu-id="c4f8c-119">容器內由 ShareName 指定的共用將會公開的路徑</span><span class="sxs-lookup"><span data-stu-id="c4f8c-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4f8c-120">-Name</span></span>
<span data-ttu-id="c4f8c-121">Azure 儲存體屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="c4f8c-122">在 Web App 或 Slot 中必須是唯一的</span><span class="sxs-lookup"><span data-stu-id="c4f8c-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c4f8c-123">-ShareName</span></span>
<span data-ttu-id="c4f8c-124">要安裝至容器的共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="c4f8c-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-125">-類型</span><span class="sxs-lookup"><span data-stu-id="c4f8c-125">-Type</span></span>
<span data-ttu-id="c4f8c-126">Azure 儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="c4f8c-127">Windows 容器僅支援 Azure 檔案</span><span class="sxs-lookup"><span data-stu-id="c4f8c-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f8c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c4f8c-128">-Confirm</span></span>
<span data-ttu-id="c4f8c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f8c-130">-WhatIf</span></span>
<span data-ttu-id="c4f8c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4f8c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f8c-133">CommonParameters</span></span>
<span data-ttu-id="c4f8c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f8c-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c4f8c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f8c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c4f8c-136">INPUTS</span></span>

### <span data-ttu-id="c4f8c-137">沒有</span><span class="sxs-lookup"><span data-stu-id="c4f8c-137">None</span></span>

## <span data-ttu-id="c4f8c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c4f8c-138">OUTPUTS</span></span>

### <span data-ttu-id="c4f8c-139">Microsoft.Azure.Commands.WebApps.models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c4f8c-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="c4f8c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c4f8c-140">NOTES</span></span>

## <span data-ttu-id="c4f8c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4f8c-141">RELATED LINKS</span></span>
