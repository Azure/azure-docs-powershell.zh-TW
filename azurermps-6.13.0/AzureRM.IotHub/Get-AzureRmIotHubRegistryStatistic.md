---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: a472ce25d648a70d9f47b6268b6bdf4f606f2a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625836"
---
# <span data-ttu-id="e5b0a-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="e5b0a-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="e5b0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b0a-103">取得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5b0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5b0a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5b0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5b0a-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b0a-106">取得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="e5b0a-107">這會在 IotHub 中提供總數、啟用及停用裝置數目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="e5b0a-108">示例</span><span class="sxs-lookup"><span data-stu-id="e5b0a-108">EXAMPLES</span></span>

### <span data-ttu-id="e5b0a-109">範例1取得 RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="e5b0a-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e5b0a-110">取得名為 "myiothub" 的 IotHub 的 RegistryStatictics</span><span class="sxs-lookup"><span data-stu-id="e5b0a-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e5b0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="e5b0a-111">PARAMETERS</span></span>

### <span data-ttu-id="e5b0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b0a-112">-DefaultProfile</span></span>
<span data-ttu-id="e5b0a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5b0a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5b0a-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5b0a-114">-Name</span></span>
<span data-ttu-id="e5b0a-115">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-115">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b0a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b0a-116">-ResourceGroupName</span></span>
<span data-ttu-id="e5b0a-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e5b0a-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b0a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b0a-118">CommonParameters</span></span>
<span data-ttu-id="e5b0a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b0a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b0a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e5b0a-121">INPUTS</span></span>

### <span data-ttu-id="e5b0a-122">System.object</span><span class="sxs-lookup"><span data-stu-id="e5b0a-122">System.String</span></span>

## <span data-ttu-id="e5b0a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e5b0a-123">OUTPUTS</span></span>

### <span data-ttu-id="e5b0a-124">PSIotHubRegistryStatistics （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="e5b0a-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="e5b0a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e5b0a-125">NOTES</span></span>

## <span data-ttu-id="e5b0a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5b0a-126">RELATED LINKS</span></span>
