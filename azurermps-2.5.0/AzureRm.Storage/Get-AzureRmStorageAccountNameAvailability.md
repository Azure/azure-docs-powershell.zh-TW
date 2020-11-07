---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
ms.openlocfilehash: 5371b5c54cfaff4b1c48dd8a8643e0cc51b1e00e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800649"
---
# <span data-ttu-id="31a87-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="31a87-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="31a87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31a87-102">SYNOPSIS</span></span>
<span data-ttu-id="31a87-103">檢查儲存空間帳戶名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="31a87-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a87-104">句法</span><span class="sxs-lookup"><span data-stu-id="31a87-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a87-105">說明</span><span class="sxs-lookup"><span data-stu-id="31a87-105">DESCRIPTION</span></span>
<span data-ttu-id="31a87-106">**AzureRmStorageAccountNameAvailability** Cmdlet 會檢查 Azure 儲存空間帳戶的名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="31a87-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="31a87-107">示例</span><span class="sxs-lookup"><span data-stu-id="31a87-107">EXAMPLES</span></span>

### <span data-ttu-id="31a87-108">範例1：檢查儲存空間帳戶名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="31a87-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="31a87-109">這個命令會檢查 name ContosoStorage03 的可用性。</span><span class="sxs-lookup"><span data-stu-id="31a87-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="31a87-110">參數</span><span class="sxs-lookup"><span data-stu-id="31a87-110">PARAMETERS</span></span>

### <span data-ttu-id="31a87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a87-111">-DefaultProfile</span></span>
<span data-ttu-id="31a87-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31a87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a87-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="31a87-113">-Name</span></span>
<span data-ttu-id="31a87-114">指定此 Cmdlet 檢查的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="31a87-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="31a87-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a87-115">CommonParameters</span></span>
<span data-ttu-id="31a87-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31a87-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a87-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31a87-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a87-118">輸入</span><span class="sxs-lookup"><span data-stu-id="31a87-118">INPUTS</span></span>

### <span data-ttu-id="31a87-119">System.object</span><span class="sxs-lookup"><span data-stu-id="31a87-119">System.String</span></span>

## <span data-ttu-id="31a87-120">輸出</span><span class="sxs-lookup"><span data-stu-id="31a87-120">OUTPUTS</span></span>

### <span data-ttu-id="31a87-121">CheckNameAvailabilityResult （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="31a87-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="31a87-122">筆記</span><span class="sxs-lookup"><span data-stu-id="31a87-122">NOTES</span></span>

## <span data-ttu-id="31a87-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="31a87-123">RELATED LINKS</span></span>

[<span data-ttu-id="31a87-124">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="31a87-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


