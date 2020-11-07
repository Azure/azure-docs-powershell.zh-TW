---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: 2343a42f3978a2811b68b4dccd50acd5f9430282
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788802"
---
# <span data-ttu-id="1fa0c-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fa0c-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="1fa0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fa0c-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa0c-103">從指定的 Azure 儲存區 blob 還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="1fa0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fa0c-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fa0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fa0c-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa0c-106">**Restore-AzApiManagement** Cmdlet 會從位於 Azurestorage blob 中的指定備份還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="1fa0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fa0c-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa0c-108">範例1：還原 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="1fa0c-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="1fa0c-109">這個命令會從 Azure 儲存區 blob 復原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="1fa0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fa0c-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa0c-111">-DefaultProfile</span></span>
<span data-ttu-id="1fa0c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa0c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fa0c-113">-Name</span></span>
<span data-ttu-id="1fa0c-114">指定將在備份中還原之 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="1fa0c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fa0c-115">-PassThru</span></span>
<span data-ttu-id="1fa0c-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1fa0c-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fa0c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa0c-118">-ResourceGroupName</span></span>
<span data-ttu-id="1fa0c-119">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="1fa0c-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="1fa0c-120">-SourceBlobName</span></span>
<span data-ttu-id="1fa0c-121">指定 Azure 儲存空間備份來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="1fa0c-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="1fa0c-122">-SourceContainerName</span></span>
<span data-ttu-id="1fa0c-123">指定 Azure 儲存空間備份來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="1fa0c-124">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="1fa0c-124">-StorageContext</span></span>
<span data-ttu-id="1fa0c-125">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="1fa0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa0c-126">CommonParameters</span></span>
<span data-ttu-id="1fa0c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa0c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa0c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1fa0c-129">INPUTS</span></span>

### <span data-ttu-id="1fa0c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1fa0c-130">System.String</span></span>

## <span data-ttu-id="1fa0c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1fa0c-131">OUTPUTS</span></span>

### <span data-ttu-id="1fa0c-132">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="1fa0c-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1fa0c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1fa0c-133">NOTES</span></span>

## <span data-ttu-id="1fa0c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fa0c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1fa0c-135">備份-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fa0c-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="1fa0c-136">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fa0c-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="1fa0c-137">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fa0c-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="1fa0c-138">移除-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1fa0c-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


