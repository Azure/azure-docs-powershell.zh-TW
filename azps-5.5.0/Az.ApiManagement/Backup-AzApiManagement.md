---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132899"
---
# <span data-ttu-id="74cfb-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74cfb-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="74cfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="74cfb-103">備份 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="74cfb-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="74cfb-104">句法</span><span class="sxs-lookup"><span data-stu-id="74cfb-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74cfb-105">說明</span><span class="sxs-lookup"><span data-stu-id="74cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="74cfb-106">**AzApiManagement** Cmdlet 會備份 Azure API 管理服務的實例。</span><span class="sxs-lookup"><span data-stu-id="74cfb-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="74cfb-107">這個 Cmdlet 會將備份儲存為 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="74cfb-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="74cfb-108">示例</span><span class="sxs-lookup"><span data-stu-id="74cfb-108">EXAMPLES</span></span>

### <span data-ttu-id="74cfb-109">範例1：備份 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="74cfb-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="74cfb-110">這個命令會將 API 管理服務備份至儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="74cfb-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="74cfb-111">參數</span><span class="sxs-lookup"><span data-stu-id="74cfb-111">PARAMETERS</span></span>

### <span data-ttu-id="74cfb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cfb-112">-DefaultProfile</span></span>
<span data-ttu-id="74cfb-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74cfb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74cfb-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="74cfb-114">-Name</span></span>
<span data-ttu-id="74cfb-115">指定此 Cmdlet 所備份之 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="74cfb-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="74cfb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74cfb-116">-PassThru</span></span>
<span data-ttu-id="74cfb-117">指示這個 Cmdlet 會傳回已備份的 **PsApiManagement** 物件（如果操作成功的話）。</span><span class="sxs-lookup"><span data-stu-id="74cfb-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="74cfb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cfb-118">-ResourceGroupName</span></span>
<span data-ttu-id="74cfb-119">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74cfb-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="74cfb-120">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="74cfb-120">-StorageContext</span></span>
<span data-ttu-id="74cfb-121">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="74cfb-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="74cfb-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="74cfb-122">-TargetBlobName</span></span>
<span data-ttu-id="74cfb-123">指定備份的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="74cfb-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="74cfb-124">如果 blob 不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="74cfb-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="74cfb-125">這個 Cmdlet 會根據下列模式產生預設值： {Name}-{yyyy MM-dd-HH-mm} apimbackup</span><span class="sxs-lookup"><span data-stu-id="74cfb-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="74cfb-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="74cfb-126">-TargetContainerName</span></span>
<span data-ttu-id="74cfb-127">指定備份之 blob 之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="74cfb-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="74cfb-128">如果容器不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="74cfb-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="74cfb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cfb-129">CommonParameters</span></span>
<span data-ttu-id="74cfb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74cfb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cfb-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74cfb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cfb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="74cfb-132">INPUTS</span></span>

### <span data-ttu-id="74cfb-133">System.object</span><span class="sxs-lookup"><span data-stu-id="74cfb-133">System.String</span></span>

### <span data-ttu-id="74cfb-134">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="74cfb-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="74cfb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="74cfb-135">OUTPUTS</span></span>

### <span data-ttu-id="74cfb-136">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="74cfb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="74cfb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="74cfb-137">NOTES</span></span>

## <span data-ttu-id="74cfb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="74cfb-138">RELATED LINKS</span></span>

[<span data-ttu-id="74cfb-139">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74cfb-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="74cfb-140">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74cfb-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="74cfb-141">移除-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74cfb-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="74cfb-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74cfb-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


