---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280118"
---
# <span data-ttu-id="0be90-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0be90-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="0be90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0be90-102">SYNOPSIS</span></span>
<span data-ttu-id="0be90-103">取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="0be90-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="0be90-104">句法</span><span class="sxs-lookup"><span data-stu-id="0be90-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be90-105">說明</span><span class="sxs-lookup"><span data-stu-id="0be90-105">DESCRIPTION</span></span>
<span data-ttu-id="0be90-106">**AzStorageUsage** Cmdlet 會取得目前訂閱之 Azure 儲存空間的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="0be90-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="0be90-107">示例</span><span class="sxs-lookup"><span data-stu-id="0be90-107">EXAMPLES</span></span>

### <span data-ttu-id="0be90-108">範例1：取得指定位置的儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="0be90-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="0be90-109">這個命令會取得目前訂閱下指定位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="0be90-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="0be90-110">參數</span><span class="sxs-lookup"><span data-stu-id="0be90-110">PARAMETERS</span></span>

### <span data-ttu-id="0be90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be90-111">-DefaultProfile</span></span>
<span data-ttu-id="0be90-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0be90-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be90-113">-位置</span><span class="sxs-lookup"><span data-stu-id="0be90-113">-Location</span></span>
<span data-ttu-id="0be90-114">指示在指定位置取得儲存資源的使用量。</span><span class="sxs-lookup"><span data-stu-id="0be90-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="0be90-115">如果未指定，將會取得訂閱下所有位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="0be90-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="0be90-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be90-116">CommonParameters</span></span>
<span data-ttu-id="0be90-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0be90-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be90-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0be90-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be90-119">輸入</span><span class="sxs-lookup"><span data-stu-id="0be90-119">INPUTS</span></span>

### <span data-ttu-id="0be90-120">System.object</span><span class="sxs-lookup"><span data-stu-id="0be90-120">System.String</span></span>

## <span data-ttu-id="0be90-121">輸出</span><span class="sxs-lookup"><span data-stu-id="0be90-121">OUTPUTS</span></span>

### <span data-ttu-id="0be90-122">PSUsage 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0be90-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="0be90-123">筆記</span><span class="sxs-lookup"><span data-stu-id="0be90-123">NOTES</span></span>

## <span data-ttu-id="0be90-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="0be90-124">RELATED LINKS</span></span>

[<span data-ttu-id="0be90-125">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0be90-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


