---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 1f0ceb4f349e7fdfee38837561dc436c16cd451b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912133"
---
# <span data-ttu-id="0b6e0-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="0b6e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6e0-103">備份 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="0b6e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="0b6e0-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b6e0-105">描述</span><span class="sxs-lookup"><span data-stu-id="0b6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0b6e0-106">**Backup-AzApiManagement** Cmdlet 可備份 Azure API 管理服務的實例。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="0b6e0-107">此 Cmdlet 將備份儲存為 Azure 儲存體 Blob。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="0b6e0-108">例子</span><span class="sxs-lookup"><span data-stu-id="0b6e0-108">EXAMPLES</span></span>

### <span data-ttu-id="0b6e0-109">範例 1：備份 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="0b6e0-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="0b6e0-110">此命令將 API 管理服務備份到儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="0b6e0-111">參數</span><span class="sxs-lookup"><span data-stu-id="0b6e0-111">PARAMETERS</span></span>

### <span data-ttu-id="0b6e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6e0-112">-DefaultProfile</span></span>
<span data-ttu-id="0b6e0-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b6e0-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b6e0-114">-Name</span></span>
<span data-ttu-id="0b6e0-115">指定此 Cmdlet 備份的 API 管理部署名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="0b6e0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b6e0-116">-PassThru</span></span>
<span data-ttu-id="0b6e0-117">表示此 Cmdlet 會返回備份 **的 PsApiManagement** 物件 ，如果作業成功。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="0b6e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b6e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b6e0-119">指定 API 管理部署存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="0b6e0-120">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0b6e0-120">-StorageContext</span></span>
<span data-ttu-id="0b6e0-121">指定儲存空間連接內容。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="0b6e0-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="0b6e0-122">-TargetBlobName</span></span>
<span data-ttu-id="0b6e0-123">指定備份的 Blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="0b6e0-124">如果 Blob 不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="0b6e0-125">此 Cmdlet 會根據下列模式產生預設值：{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="0b6e0-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="0b6e0-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="0b6e0-126">-TargetContainerName</span></span>
<span data-ttu-id="0b6e0-127">指定備份時 Blob 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="0b6e0-128">如果容器不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="0b6e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6e0-129">CommonParameters</span></span>
<span data-ttu-id="0b6e0-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b6e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6e0-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b6e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6e0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0b6e0-132">INPUTS</span></span>

### <span data-ttu-id="0b6e0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0b6e0-133">System.String</span></span>

### <span data-ttu-id="0b6e0-134">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0b6e0-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b6e0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0b6e0-135">OUTPUTS</span></span>

### <span data-ttu-id="0b6e0-136">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0b6e0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0b6e0-137">NOTES</span></span>

## <span data-ttu-id="0b6e0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b6e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="0b6e0-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="0b6e0-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0b6e0-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="0b6e0-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b6e0-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


