---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795119"
---
# <span data-ttu-id="592a6-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="592a6-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="592a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="592a6-102">SYNOPSIS</span></span>
<span data-ttu-id="592a6-103">取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="592a6-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="592a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="592a6-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="592a6-105">DESCRIPTION</span></span>
<span data-ttu-id="592a6-106">**AzStorageUsage** Cmdlet 會取得目前訂閱之 Azure 儲存空間的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="592a6-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="592a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="592a6-107">EXAMPLES</span></span>

### <span data-ttu-id="592a6-108">範例1：取得儲存資源使用量</span><span class="sxs-lookup"><span data-stu-id="592a6-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="592a6-109">這個命令會取得目前訂閱的儲存資源使用量。</span><span class="sxs-lookup"><span data-stu-id="592a6-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="592a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="592a6-110">PARAMETERS</span></span>

### <span data-ttu-id="592a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a6-111">-DefaultProfile</span></span>
<span data-ttu-id="592a6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="592a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592a6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a6-113">CommonParameters</span></span>
<span data-ttu-id="592a6-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="592a6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a6-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="592a6-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a6-116">輸入</span><span class="sxs-lookup"><span data-stu-id="592a6-116">INPUTS</span></span>

### <span data-ttu-id="592a6-117">所有</span><span class="sxs-lookup"><span data-stu-id="592a6-117">None</span></span>

## <span data-ttu-id="592a6-118">輸出</span><span class="sxs-lookup"><span data-stu-id="592a6-118">OUTPUTS</span></span>

### <span data-ttu-id="592a6-119">PSUsage 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="592a6-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="592a6-120">筆記</span><span class="sxs-lookup"><span data-stu-id="592a6-120">NOTES</span></span>

## <span data-ttu-id="592a6-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="592a6-121">RELATED LINKS</span></span>

[<span data-ttu-id="592a6-122">Azure 儲存管理器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="592a6-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


