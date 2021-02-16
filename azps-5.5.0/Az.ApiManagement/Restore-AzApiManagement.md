---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137591"
---
# <span data-ttu-id="140d6-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="140d6-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="140d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="140d6-102">SYNOPSIS</span></span>
<span data-ttu-id="140d6-103">從指定的 Azure 儲存區 blob 還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="140d6-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="140d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="140d6-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="140d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="140d6-105">DESCRIPTION</span></span>
<span data-ttu-id="140d6-106">**Restore-AzApiManagement** Cmdlet 會從位於 Azurestorage blob 中的指定備份還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="140d6-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="140d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="140d6-107">EXAMPLES</span></span>

### <span data-ttu-id="140d6-108">範例1：還原 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="140d6-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="140d6-109">這個命令會從 Azure 儲存區 blob 復原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="140d6-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="140d6-110">參數</span><span class="sxs-lookup"><span data-stu-id="140d6-110">PARAMETERS</span></span>

### <span data-ttu-id="140d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140d6-111">-DefaultProfile</span></span>
<span data-ttu-id="140d6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="140d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="140d6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="140d6-113">-Name</span></span>
<span data-ttu-id="140d6-114">指定將在備份中還原之 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="140d6-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="140d6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="140d6-115">-PassThru</span></span>
<span data-ttu-id="140d6-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="140d6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="140d6-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="140d6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="140d6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140d6-118">-ResourceGroupName</span></span>
<span data-ttu-id="140d6-119">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="140d6-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="140d6-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="140d6-120">-SourceBlobName</span></span>
<span data-ttu-id="140d6-121">指定 Azure 儲存空間備份來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="140d6-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="140d6-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="140d6-122">-SourceContainerName</span></span>
<span data-ttu-id="140d6-123">指定 Azure 儲存空間備份來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="140d6-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="140d6-124">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="140d6-124">-StorageContext</span></span>
<span data-ttu-id="140d6-125">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="140d6-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="140d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140d6-126">CommonParameters</span></span>
<span data-ttu-id="140d6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="140d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140d6-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="140d6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140d6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="140d6-129">INPUTS</span></span>

### <span data-ttu-id="140d6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="140d6-130">System.String</span></span>

## <span data-ttu-id="140d6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="140d6-131">OUTPUTS</span></span>

### <span data-ttu-id="140d6-132">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="140d6-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="140d6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="140d6-133">NOTES</span></span>

## <span data-ttu-id="140d6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="140d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="140d6-135">備份-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="140d6-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="140d6-136">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="140d6-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="140d6-137">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="140d6-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="140d6-138">移除-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="140d6-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


