---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d1c7e1938d50e4a970dbec15568bc5cf10257639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916301"
---
# <span data-ttu-id="b7135-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="b7135-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7135-102">SYNOPSIS</span></span>
<span data-ttu-id="b7135-103">從指定的 Azure 儲存 Blob 還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="b7135-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="b7135-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7135-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7135-105">描述</span><span class="sxs-lookup"><span data-stu-id="b7135-105">DESCRIPTION</span></span>
<span data-ttu-id="b7135-106">**Restore-AzApiManagement** Cmdlet 會從位於 Azurestorage Blob 中的指定備份還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="b7135-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="b7135-107">例子</span><span class="sxs-lookup"><span data-stu-id="b7135-107">EXAMPLES</span></span>

### <span data-ttu-id="b7135-108">範例 1：還原 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="b7135-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="b7135-109">此命令會從 Azure 儲存 Blob 還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="b7135-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="b7135-110">參數</span><span class="sxs-lookup"><span data-stu-id="b7135-110">PARAMETERS</span></span>

### <span data-ttu-id="b7135-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7135-111">-DefaultProfile</span></span>
<span data-ttu-id="b7135-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7135-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7135-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7135-113">-Name</span></span>
<span data-ttu-id="b7135-114">指定將隨備份一起還原的 API 管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b7135-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7135-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7135-115">-PassThru</span></span>
<span data-ttu-id="b7135-116">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b7135-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7135-117">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b7135-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7135-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7135-118">-ResourceGroupName</span></span>
<span data-ttu-id="b7135-119">指定 API 管理存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7135-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7135-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="b7135-120">-SourceBlobName</span></span>
<span data-ttu-id="b7135-121">指定 Azure 儲存備份來源 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7135-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7135-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="b7135-122">-SourceContainerName</span></span>
<span data-ttu-id="b7135-123">指定 Azure 儲存備份來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7135-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7135-124">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b7135-124">-StorageContext</span></span>
<span data-ttu-id="b7135-125">指定儲存空間連接內容。</span><span class="sxs-lookup"><span data-stu-id="b7135-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7135-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7135-126">CommonParameters</span></span>
<span data-ttu-id="b7135-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7135-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7135-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7135-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7135-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b7135-129">INPUTS</span></span>

### <span data-ttu-id="b7135-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b7135-130">System.String</span></span>

## <span data-ttu-id="b7135-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b7135-131">OUTPUTS</span></span>

### <span data-ttu-id="b7135-132">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b7135-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b7135-133">NOTES</span></span>

## <span data-ttu-id="b7135-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7135-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7135-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="b7135-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="b7135-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="b7135-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7135-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


