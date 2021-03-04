---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 9e12aa08bd37a5dfa467b2df03df42f5c58e4186
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912989"
---
# <span data-ttu-id="3431a-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3431a-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="3431a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3431a-102">SYNOPSIS</span></span>
<span data-ttu-id="3431a-103">獲得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3431a-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="3431a-104">語法</span><span class="sxs-lookup"><span data-stu-id="3431a-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3431a-105">描述</span><span class="sxs-lookup"><span data-stu-id="3431a-105">DESCRIPTION</span></span>
<span data-ttu-id="3431a-106">**Get-AzStorageUsage Cmdlet** 會取得目前訂閱 Azure 儲存空間的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3431a-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="3431a-107">例子</span><span class="sxs-lookup"><span data-stu-id="3431a-107">EXAMPLES</span></span>

### <span data-ttu-id="3431a-108">範例 1：取得指定位置的儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="3431a-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="3431a-109">此命令會獲得目前訂閱下指定位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3431a-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="3431a-110">參數</span><span class="sxs-lookup"><span data-stu-id="3431a-110">PARAMETERS</span></span>

### <span data-ttu-id="3431a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3431a-111">-DefaultProfile</span></span>
<span data-ttu-id="3431a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3431a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3431a-113">-位置</span><span class="sxs-lookup"><span data-stu-id="3431a-113">-Location</span></span>
<span data-ttu-id="3431a-114">指出要取得指定位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3431a-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="3431a-115">如果未指定，將會取得訂閱下所有位置的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3431a-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="3431a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3431a-116">CommonParameters</span></span>
<span data-ttu-id="3431a-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3431a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3431a-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3431a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3431a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3431a-119">INPUTS</span></span>

### <span data-ttu-id="3431a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="3431a-120">System.String</span></span>

## <span data-ttu-id="3431a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="3431a-121">OUTPUTS</span></span>

### <span data-ttu-id="3431a-122">Microsoft.Azure.Commands.management.storage.models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="3431a-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="3431a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3431a-123">NOTES</span></span>

## <span data-ttu-id="3431a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="3431a-124">RELATED LINKS</span></span>

[<span data-ttu-id="3431a-125">Azure 儲存體管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3431a-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


