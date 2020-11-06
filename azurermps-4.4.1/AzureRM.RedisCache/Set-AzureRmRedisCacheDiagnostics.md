---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455616"
---
# <span data-ttu-id="1da96-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1da96-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="1da96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1da96-102">SYNOPSIS</span></span>
<span data-ttu-id="1da96-103">啟用 Azure Redis Cache 的診斷。</span><span class="sxs-lookup"><span data-stu-id="1da96-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da96-104">句法</span><span class="sxs-lookup"><span data-stu-id="1da96-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da96-105">說明</span><span class="sxs-lookup"><span data-stu-id="1da96-105">DESCRIPTION</span></span>
<span data-ttu-id="1da96-106">**AzureRmRedisCacheDiagnostics** Cmdlet 可為 Azure Redis Cache 啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="1da96-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="1da96-107">示例</span><span class="sxs-lookup"><span data-stu-id="1da96-107">EXAMPLES</span></span>

### <span data-ttu-id="1da96-108">範例1：啟用診斷</span><span class="sxs-lookup"><span data-stu-id="1da96-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="1da96-109">這個命令會啟用 Azure Redis 快取的診斷。</span><span class="sxs-lookup"><span data-stu-id="1da96-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="1da96-110">此命令將針對訂閱的同一區域中的所有 Azure Redis 緩存啟用診斷或更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1da96-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="1da96-111">參數</span><span class="sxs-lookup"><span data-stu-id="1da96-111">PARAMETERS</span></span>

### <span data-ttu-id="1da96-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="1da96-112">-Name</span></span>
<span data-ttu-id="1da96-113">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="1da96-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="1da96-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da96-114">-ResourceGroupName</span></span>
<span data-ttu-id="1da96-115">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1da96-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="1da96-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1da96-116">-StorageAccountId</span></span>
<span data-ttu-id="1da96-117">指定用來儲存診斷資料之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1da96-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="1da96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da96-118">-DefaultProfile</span></span>
<span data-ttu-id="1da96-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1da96-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da96-120">CommonParameters</span></span>
<span data-ttu-id="1da96-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1da96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da96-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1da96-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da96-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1da96-123">INPUTS</span></span>

### <span data-ttu-id="1da96-124">所有</span><span class="sxs-lookup"><span data-stu-id="1da96-124">None</span></span>

## <span data-ttu-id="1da96-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1da96-125">OUTPUTS</span></span>

### <span data-ttu-id="1da96-126">失去</span><span class="sxs-lookup"><span data-stu-id="1da96-126">Void</span></span>

## <span data-ttu-id="1da96-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1da96-127">NOTES</span></span>
* <span data-ttu-id="1da96-128">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="1da96-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1da96-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1da96-129">RELATED LINKS</span></span>

[<span data-ttu-id="1da96-130">移除-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1da96-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


