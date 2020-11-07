---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623522"
---
# <span data-ttu-id="781e0-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="781e0-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="781e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="781e0-102">SYNOPSIS</span></span>
<span data-ttu-id="781e0-103">從指定的 Azure 儲存區 blob 還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="781e0-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="781e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="781e0-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="781e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="781e0-105">DESCRIPTION</span></span>
<span data-ttu-id="781e0-106">**Restore-AzureRmApiManagement** Cmdlet 會從位於 Azurestorage blob 中的指定備份還原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="781e0-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="781e0-107">示例</span><span class="sxs-lookup"><span data-stu-id="781e0-107">EXAMPLES</span></span>

### <span data-ttu-id="781e0-108">範例1：還原 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="781e0-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="781e0-109">這個命令會從 Azure 儲存區 blob 復原 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="781e0-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="781e0-110">參數</span><span class="sxs-lookup"><span data-stu-id="781e0-110">PARAMETERS</span></span>

### <span data-ttu-id="781e0-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="781e0-111">-Name</span></span>
<span data-ttu-id="781e0-112">指定將在備份中還原之 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="781e0-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="781e0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="781e0-113">-PassThru</span></span>
<span data-ttu-id="781e0-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="781e0-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="781e0-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="781e0-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="781e0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781e0-116">-ResourceGroupName</span></span>
<span data-ttu-id="781e0-117">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="781e0-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="781e0-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="781e0-118">-SourceBlobName</span></span>
<span data-ttu-id="781e0-119">指定 Azure 儲存空間備份來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="781e0-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="781e0-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="781e0-120">-SourceContainerName</span></span>
<span data-ttu-id="781e0-121">指定 Azure 儲存空間備份來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="781e0-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="781e0-122">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="781e0-122">-StorageContext</span></span>
<span data-ttu-id="781e0-123">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="781e0-123">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="781e0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781e0-124">-DefaultProfile</span></span>
<span data-ttu-id="781e0-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="781e0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="781e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781e0-126">CommonParameters</span></span>
<span data-ttu-id="781e0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="781e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781e0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="781e0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781e0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="781e0-129">INPUTS</span></span>

## <span data-ttu-id="781e0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="781e0-130">OUTPUTS</span></span>

### <span data-ttu-id="781e0-131">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="781e0-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="781e0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="781e0-132">NOTES</span></span>

## <span data-ttu-id="781e0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="781e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="781e0-134">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="781e0-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="781e0-135">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="781e0-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="781e0-136">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="781e0-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="781e0-137">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="781e0-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


