---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 6e4582a8963f3d57bacd3dfb9c869368986c5668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915149"
---
# <span data-ttu-id="54891-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="54891-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="54891-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54891-102">SYNOPSIS</span></span>
<span data-ttu-id="54891-103">檢查儲存空間帳戶名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="54891-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="54891-104">語法</span><span class="sxs-lookup"><span data-stu-id="54891-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54891-105">描述</span><span class="sxs-lookup"><span data-stu-id="54891-105">DESCRIPTION</span></span>
<span data-ttu-id="54891-106">**Get-AzStorageAccountNameAvailability Cmdlet** 會檢查 Azure 儲存體帳戶的名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="54891-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="54891-107">例子</span><span class="sxs-lookup"><span data-stu-id="54891-107">EXAMPLES</span></span>

### <span data-ttu-id="54891-108">範例 1：檢查儲存空間帳戶名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="54891-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="54891-109">此命令會檢查 ContosoStorage03 名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="54891-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="54891-110">參數</span><span class="sxs-lookup"><span data-stu-id="54891-110">PARAMETERS</span></span>

### <span data-ttu-id="54891-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54891-111">-DefaultProfile</span></span>
<span data-ttu-id="54891-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54891-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54891-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="54891-113">-Name</span></span>
<span data-ttu-id="54891-114">指定此 Cmdlet 檢查的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="54891-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54891-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54891-115">CommonParameters</span></span>
<span data-ttu-id="54891-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54891-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54891-117">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="54891-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54891-118">輸入</span><span class="sxs-lookup"><span data-stu-id="54891-118">INPUTS</span></span>

### <span data-ttu-id="54891-119">System.String</span><span class="sxs-lookup"><span data-stu-id="54891-119">System.String</span></span>

## <span data-ttu-id="54891-120">輸出</span><span class="sxs-lookup"><span data-stu-id="54891-120">OUTPUTS</span></span>

### <span data-ttu-id="54891-121">Microsoft.Azure.management.storage.models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="54891-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="54891-122">筆記</span><span class="sxs-lookup"><span data-stu-id="54891-122">NOTES</span></span>

## <span data-ttu-id="54891-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="54891-123">RELATED LINKS</span></span>

[<span data-ttu-id="54891-124">Azure 儲存體管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54891-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


