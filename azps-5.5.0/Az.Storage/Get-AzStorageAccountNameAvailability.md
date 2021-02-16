---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139682"
---
# <span data-ttu-id="c6aa7-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c6aa7-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="c6aa7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aa7-103">檢查儲存空間帳戶名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="c6aa7-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6aa7-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6aa7-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="c6aa7-106">**AzStorageAccountNameAvailability** Cmdlet 會檢查 Azure 儲存空間帳戶的名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="c6aa7-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6aa7-107">EXAMPLES</span></span>

### <span data-ttu-id="c6aa7-108">範例1：檢查儲存空間帳戶名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="c6aa7-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="c6aa7-109">這個命令會檢查 name ContosoStorage03 的可用性。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="c6aa7-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6aa7-110">PARAMETERS</span></span>

### <span data-ttu-id="c6aa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6aa7-111">-DefaultProfile</span></span>
<span data-ttu-id="c6aa7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6aa7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6aa7-113">-Name</span></span>
<span data-ttu-id="c6aa7-114">指定此 Cmdlet 檢查的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="c6aa7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aa7-115">CommonParameters</span></span>
<span data-ttu-id="c6aa7-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aa7-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aa7-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c6aa7-118">INPUTS</span></span>

### <span data-ttu-id="c6aa7-119">System.object</span><span class="sxs-lookup"><span data-stu-id="c6aa7-119">System.String</span></span>

## <span data-ttu-id="c6aa7-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c6aa7-120">OUTPUTS</span></span>

### <span data-ttu-id="c6aa7-121">CheckNameAvailabilityResult （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c6aa7-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="c6aa7-122">筆記</span><span class="sxs-lookup"><span data-stu-id="c6aa7-122">NOTES</span></span>

## <span data-ttu-id="c6aa7-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6aa7-123">RELATED LINKS</span></span>

[<span data-ttu-id="c6aa7-124">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6aa7-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


