---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452635"
---
# <span data-ttu-id="407b3-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="407b3-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="407b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="407b3-102">SYNOPSIS</span></span>
<span data-ttu-id="407b3-103">備份 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="407b3-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="407b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="407b3-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="407b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="407b3-105">DESCRIPTION</span></span>
<span data-ttu-id="407b3-106">**AzureRmApiManagement** Cmdlet 會備份 Azure API 管理服務的實例。</span><span class="sxs-lookup"><span data-stu-id="407b3-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="407b3-107">這個 Cmdlet 會將備份儲存為 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="407b3-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="407b3-108">示例</span><span class="sxs-lookup"><span data-stu-id="407b3-108">EXAMPLES</span></span>

### <span data-ttu-id="407b3-109">範例1：備份 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="407b3-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="407b3-110">這個命令會將 API 管理服務備份至儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="407b3-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="407b3-111">參數</span><span class="sxs-lookup"><span data-stu-id="407b3-111">PARAMETERS</span></span>

### <span data-ttu-id="407b3-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="407b3-112">-Name</span></span>
<span data-ttu-id="407b3-113">指定此 Cmdlet 所備份之 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="407b3-113">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="407b3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="407b3-114">-PassThru</span></span>
<span data-ttu-id="407b3-115">指示這個 Cmdlet 會傳回已備份的 **PsApiManagement** 物件（如果操作成功的話）。</span><span class="sxs-lookup"><span data-stu-id="407b3-115">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="407b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="407b3-117">指定 API 管理部署所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="407b3-117">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="407b3-118">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="407b3-118">-StorageContext</span></span>
<span data-ttu-id="407b3-119">指定儲存連接內容。</span><span class="sxs-lookup"><span data-stu-id="407b3-119">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="407b3-120">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="407b3-120">-TargetBlobName</span></span>
<span data-ttu-id="407b3-121">指定備份的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="407b3-121">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="407b3-122">如果 blob 不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="407b3-122">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="407b3-123">這個 Cmdlet 會根據下列模式產生預設值：</span><span class="sxs-lookup"><span data-stu-id="407b3-123">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="407b3-124">{Name}-{yyyy-mm-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="407b3-124">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="407b3-125">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="407b3-125">-TargetContainerName</span></span>
<span data-ttu-id="407b3-126">指定備份之 blob 之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="407b3-126">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="407b3-127">如果容器不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="407b3-127">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="407b3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407b3-128">-DefaultProfile</span></span>
<span data-ttu-id="407b3-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="407b3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="407b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407b3-130">CommonParameters</span></span>
<span data-ttu-id="407b3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="407b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407b3-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="407b3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407b3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="407b3-133">INPUTS</span></span>

## <span data-ttu-id="407b3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="407b3-134">OUTPUTS</span></span>

### <span data-ttu-id="407b3-135">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="407b3-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="407b3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="407b3-136">NOTES</span></span>

## <span data-ttu-id="407b3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="407b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="407b3-138">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="407b3-138">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="407b3-139">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="407b3-139">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="407b3-140">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="407b3-140">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="407b3-141">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="407b3-141">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


