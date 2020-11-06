---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452911"
---
# <span data-ttu-id="85e31-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="85e31-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="85e31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85e31-102">SYNOPSIS</span></span>
<span data-ttu-id="85e31-103">備份 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="85e31-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85e31-104">句法</span><span class="sxs-lookup"><span data-stu-id="85e31-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85e31-105">說明</span><span class="sxs-lookup"><span data-stu-id="85e31-105">DESCRIPTION</span></span>
<span data-ttu-id="85e31-106">**AzureRmApiManagement** Cmdlet 會備份 Azure API 管理服務的實例。</span><span class="sxs-lookup"><span data-stu-id="85e31-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="85e31-107">這個 Cmdlet 會將備份儲存為 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="85e31-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="85e31-108">示例</span><span class="sxs-lookup"><span data-stu-id="85e31-108">EXAMPLES</span></span>

### <span data-ttu-id="85e31-109">範例1：備份 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="85e31-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="85e31-110">這個命令會將 API 管理服務備份至儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="85e31-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="85e31-111">參數</span><span class="sxs-lookup"><span data-stu-id="85e31-111">PARAMETERS</span></span>

### <span data-ttu-id="85e31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e31-112">-DefaultProfile</span></span>
<span data-ttu-id="85e31-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85e31-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85e31-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="85e31-114">-Name</span></span>
<span data-ttu-id="85e31-115">指定此 Cmdlet 所備份之 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="85e31-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="85e31-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85e31-116">-PassThru</span></span>
<span data-ttu-id="85e31-117">指示這個 Cmdlet 會傳回已備份的 **PsApiManagement** 物件（如果操作成功的話）。</span><span class="sxs-lookup"><span data-stu-id="85e31-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="85e31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e31-118">-ResourceGroupName</span></span>
<span data-ttu-id="85e31-119">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85e31-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="85e31-120">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="85e31-120">-StorageContext</span></span>
<span data-ttu-id="85e31-121">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="85e31-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e31-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="85e31-122">-TargetBlobName</span></span>
<span data-ttu-id="85e31-123">指定備份的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="85e31-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="85e31-124">如果 blob 不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="85e31-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="85e31-125">這個 Cmdlet 會根據下列模式產生預設值： {Name}-{yyyy MM-dd-HH-mm} apimbackup</span><span class="sxs-lookup"><span data-stu-id="85e31-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e31-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="85e31-126">-TargetContainerName</span></span>
<span data-ttu-id="85e31-127">指定備份之 blob 之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="85e31-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="85e31-128">如果容器不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="85e31-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="85e31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e31-129">CommonParameters</span></span>
<span data-ttu-id="85e31-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85e31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e31-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85e31-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e31-132">輸入</span><span class="sxs-lookup"><span data-stu-id="85e31-132">INPUTS</span></span>

### <span data-ttu-id="85e31-133">System.object</span><span class="sxs-lookup"><span data-stu-id="85e31-133">System.String</span></span>

### <span data-ttu-id="85e31-134">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="85e31-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="85e31-135">輸出</span><span class="sxs-lookup"><span data-stu-id="85e31-135">OUTPUTS</span></span>

### <span data-ttu-id="85e31-136">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="85e31-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="85e31-137">筆記</span><span class="sxs-lookup"><span data-stu-id="85e31-137">NOTES</span></span>

## <span data-ttu-id="85e31-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="85e31-138">RELATED LINKS</span></span>

[<span data-ttu-id="85e31-139">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="85e31-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="85e31-140">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="85e31-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="85e31-141">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="85e31-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="85e31-142">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="85e31-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


