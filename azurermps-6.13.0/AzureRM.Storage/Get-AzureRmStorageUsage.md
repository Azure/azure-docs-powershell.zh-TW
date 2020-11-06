---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450161"
---
# <span data-ttu-id="84959-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="84959-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="84959-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84959-102">SYNOPSIS</span></span>
<span data-ttu-id="84959-103">取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84959-104">句法</span><span class="sxs-lookup"><span data-stu-id="84959-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84959-105">說明</span><span class="sxs-lookup"><span data-stu-id="84959-105">DESCRIPTION</span></span>
<span data-ttu-id="84959-106">**AzureRmStorageUsage** Cmdlet 會取得目前訂閱之 Azure 儲存空間的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="84959-107">示例</span><span class="sxs-lookup"><span data-stu-id="84959-107">EXAMPLES</span></span>

### <span data-ttu-id="84959-108">範例1：取得儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="84959-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="84959-109">這個命令會取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="84959-110">範例2：取得指定位置的儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="84959-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="84959-111">這個命令會在目前的訂閱下，取得指定位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="84959-112">參數</span><span class="sxs-lookup"><span data-stu-id="84959-112">PARAMETERS</span></span>

### <span data-ttu-id="84959-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84959-113">-DefaultProfile</span></span>
<span data-ttu-id="84959-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84959-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84959-115">-位置</span><span class="sxs-lookup"><span data-stu-id="84959-115">-Location</span></span>
<span data-ttu-id="84959-116">指示在指定位置取得儲存資源的使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="84959-117">如果未指定，將會取得訂閱下所有位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="84959-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84959-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84959-118">CommonParameters</span></span>
<span data-ttu-id="84959-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84959-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84959-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84959-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84959-121">輸入</span><span class="sxs-lookup"><span data-stu-id="84959-121">INPUTS</span></span>

### <span data-ttu-id="84959-122">所有</span><span class="sxs-lookup"><span data-stu-id="84959-122">None</span></span>

## <span data-ttu-id="84959-123">輸出</span><span class="sxs-lookup"><span data-stu-id="84959-123">OUTPUTS</span></span>

### <span data-ttu-id="84959-124">PSUsage 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="84959-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="84959-125">筆記</span><span class="sxs-lookup"><span data-stu-id="84959-125">NOTES</span></span>

## <span data-ttu-id="84959-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="84959-126">RELATED LINKS</span></span>

[<span data-ttu-id="84959-127">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="84959-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


