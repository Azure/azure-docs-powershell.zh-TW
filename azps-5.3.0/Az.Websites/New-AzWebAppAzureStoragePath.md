---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436001"
---
# <span data-ttu-id="8d32f-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8d32f-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="8d32f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d32f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d32f-103">建立代表要在 Web App 中裝載之 Azure 儲存路徑的物件。</span><span class="sxs-lookup"><span data-stu-id="8d32f-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="8d32f-104">它是用來做為 Set-AzWebApp 與 Set-AzWebAppSlot ( AzureStoragePath) 的參數</span><span class="sxs-lookup"><span data-stu-id="8d32f-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8d32f-105">句法</span><span class="sxs-lookup"><span data-stu-id="8d32f-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d32f-106">說明</span><span class="sxs-lookup"><span data-stu-id="8d32f-106">DESCRIPTION</span></span>
<span data-ttu-id="8d32f-107">建立代表要在 Web App 內裝載之 Azure 儲存路徑的物件。</span><span class="sxs-lookup"><span data-stu-id="8d32f-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="8d32f-108">示例</span><span class="sxs-lookup"><span data-stu-id="8d32f-108">EXAMPLES</span></span>

### <span data-ttu-id="8d32f-109">範例1</span><span class="sxs-lookup"><span data-stu-id="8d32f-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="8d32f-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d32f-110">PARAMETERS</span></span>

### <span data-ttu-id="8d32f-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="8d32f-111">-AccessKey</span></span>
<span data-ttu-id="8d32f-112">Azure 儲存空間帳戶的存取金鑰</span><span class="sxs-lookup"><span data-stu-id="8d32f-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="8d32f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d32f-113">-AccountName</span></span>
<span data-ttu-id="8d32f-114">Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8d32f-114">Azure Storage account name.</span></span>
<span data-ttu-id="8d32f-115">例如： myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="8d32f-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="8d32f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d32f-116">-DefaultProfile</span></span>
<span data-ttu-id="8d32f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d32f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d32f-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="8d32f-118">-MountPath</span></span>
<span data-ttu-id="8d32f-119">容器中由共用指定的共用將會公開的路徑</span><span class="sxs-lookup"><span data-stu-id="8d32f-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="8d32f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d32f-120">-Name</span></span>
<span data-ttu-id="8d32f-121">Azure 儲存空間屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d32f-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="8d32f-122">在 Web 應用程式或槽中必須是唯一的</span><span class="sxs-lookup"><span data-stu-id="8d32f-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="8d32f-123">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="8d32f-123">-ShareName</span></span>
<span data-ttu-id="8d32f-124">要裝載至容器的共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="8d32f-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="8d32f-125">-類型</span><span class="sxs-lookup"><span data-stu-id="8d32f-125">-Type</span></span>
<span data-ttu-id="8d32f-126">Azure 儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="8d32f-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="8d32f-127">Windows 容器只支援 Azure 檔案</span><span class="sxs-lookup"><span data-stu-id="8d32f-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="8d32f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8d32f-128">-Confirm</span></span>
<span data-ttu-id="8d32f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d32f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d32f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d32f-130">-WhatIf</span></span>
<span data-ttu-id="8d32f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d32f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d32f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d32f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d32f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d32f-133">CommonParameters</span></span>
<span data-ttu-id="8d32f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d32f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d32f-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d32f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d32f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8d32f-136">INPUTS</span></span>

### <span data-ttu-id="8d32f-137">所有</span><span class="sxs-lookup"><span data-stu-id="8d32f-137">None</span></span>

## <span data-ttu-id="8d32f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8d32f-138">OUTPUTS</span></span>

### <span data-ttu-id="8d32f-139">WebAppAzureStoragePath 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="8d32f-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="8d32f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8d32f-140">NOTES</span></span>

## <span data-ttu-id="8d32f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d32f-141">RELATED LINKS</span></span>
