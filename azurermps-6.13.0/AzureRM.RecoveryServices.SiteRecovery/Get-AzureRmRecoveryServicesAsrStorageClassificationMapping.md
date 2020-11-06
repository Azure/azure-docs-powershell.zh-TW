---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: ec5ba90fd0c3dbdbf96ddf2370948de090306611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455108"
---
# <span data-ttu-id="05cb3-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="05cb3-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="05cb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="05cb3-103">取得 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="05cb3-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05cb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="05cb3-104">SYNTAX</span></span>

### <span data-ttu-id="05cb3-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="05cb3-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05cb3-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="05cb3-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05cb3-107">說明</span><span class="sxs-lookup"><span data-stu-id="05cb3-107">DESCRIPTION</span></span>
<span data-ttu-id="05cb3-108">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會取得 ASR 儲存分類對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="05cb3-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="05cb3-109">示例</span><span class="sxs-lookup"><span data-stu-id="05cb3-109">EXAMPLES</span></span>

### <span data-ttu-id="05cb3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="05cb3-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="05cb3-111">列出與指定的儲存分類相關的所有儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="05cb3-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="05cb3-112">參數</span><span class="sxs-lookup"><span data-stu-id="05cb3-112">PARAMETERS</span></span>

### <span data-ttu-id="05cb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cb3-113">-DefaultProfile</span></span>
<span data-ttu-id="05cb3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05cb3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="05cb3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="05cb3-115">-Name</span></span>
<span data-ttu-id="05cb3-116">指定要取得之儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="05cb3-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cb3-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="05cb3-117">-StorageClassification</span></span>
<span data-ttu-id="05cb3-118">指定 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="05cb3-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="05cb3-119">這個 Cmdlet 會取得與指定的儲存分類相對應的 ASR 儲存分類對應</span><span class="sxs-lookup"><span data-stu-id="05cb3-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cb3-120">CommonParameters</span></span>
<span data-ttu-id="05cb3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05cb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cb3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05cb3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cb3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="05cb3-123">INPUTS</span></span>

### <span data-ttu-id="05cb3-124">所有</span><span class="sxs-lookup"><span data-stu-id="05cb3-124">None</span></span>

## <span data-ttu-id="05cb3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="05cb3-125">OUTPUTS</span></span>

### <span data-ttu-id="05cb3-126">System.object. IEnumerable "1 [ASRStorageClassificationMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="05cb3-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="05cb3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="05cb3-127">NOTES</span></span>

## <span data-ttu-id="05cb3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="05cb3-128">RELATED LINKS</span></span>

[<span data-ttu-id="05cb3-129">新-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="05cb3-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="05cb3-130">移除-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="05cb3-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
