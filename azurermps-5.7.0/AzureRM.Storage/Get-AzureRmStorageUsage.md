---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: 5d44fa0a3e0ead373a822ae91080df9bdc60cc50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452987"
---
# <span data-ttu-id="3d002-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3d002-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="3d002-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d002-102">SYNOPSIS</span></span>
<span data-ttu-id="3d002-103">取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3d002-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d002-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d002-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d002-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d002-105">DESCRIPTION</span></span>
<span data-ttu-id="3d002-106">**AzureRmStorageUsage** Cmdlet 會取得目前訂閱之 Azure 儲存空間的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3d002-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="3d002-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d002-107">EXAMPLES</span></span>

### <span data-ttu-id="3d002-108">範例1：取得儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="3d002-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="3d002-109">這個命令會取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="3d002-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="3d002-110">參數</span><span class="sxs-lookup"><span data-stu-id="3d002-110">PARAMETERS</span></span>

### <span data-ttu-id="3d002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d002-111">-DefaultProfile</span></span>
<span data-ttu-id="3d002-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d002-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d002-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d002-113">CommonParameters</span></span>
<span data-ttu-id="3d002-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d002-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d002-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d002-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d002-116">輸入</span><span class="sxs-lookup"><span data-stu-id="3d002-116">INPUTS</span></span>

### <span data-ttu-id="3d002-117">所有</span><span class="sxs-lookup"><span data-stu-id="3d002-117">None</span></span>
<span data-ttu-id="3d002-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3d002-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d002-119">輸出</span><span class="sxs-lookup"><span data-stu-id="3d002-119">OUTPUTS</span></span>

### <span data-ttu-id="3d002-120">PSUsage 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3d002-120">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="3d002-121">筆記</span><span class="sxs-lookup"><span data-stu-id="3d002-121">NOTES</span></span>

## <span data-ttu-id="3d002-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d002-122">RELATED LINKS</span></span>

[<span data-ttu-id="3d002-123">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d002-123">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)

