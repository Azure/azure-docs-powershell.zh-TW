---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449345"
---
# <span data-ttu-id="ba979-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="ba979-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="ba979-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba979-102">SYNOPSIS</span></span>
<span data-ttu-id="ba979-103">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="ba979-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba979-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba979-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba979-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba979-105">DESCRIPTION</span></span>
<span data-ttu-id="ba979-106">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="ba979-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="ba979-107">您可以為所有的按鍵取得 connectionstrings，或使用特定的金鑰名稱進行篩選。</span><span class="sxs-lookup"><span data-stu-id="ba979-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="ba979-108">示例</span><span class="sxs-lookup"><span data-stu-id="ba979-108">EXAMPLES</span></span>

### <span data-ttu-id="ba979-109">範例1取得所有 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="ba979-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ba979-110">取得名為 "myiothub" 的 iothub 所有鍵的 connectionstrings</span><span class="sxs-lookup"><span data-stu-id="ba979-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="ba979-111">範例2取得特定金鑰的 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="ba979-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="ba979-112">針對名為 "myiothub" 的 iothub，取得名為 "mykey" 之金鑰的 connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="ba979-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="ba979-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba979-113">PARAMETERS</span></span>

### <span data-ttu-id="ba979-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba979-114">-DefaultProfile</span></span>
<span data-ttu-id="ba979-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ba979-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba979-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ba979-116">-KeyName</span></span>
<span data-ttu-id="ba979-117">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="ba979-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba979-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba979-118">-Name</span></span>
<span data-ttu-id="ba979-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ba979-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba979-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba979-120">-ResourceGroupName</span></span>
<span data-ttu-id="ba979-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ba979-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba979-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba979-122">CommonParameters</span></span>
<span data-ttu-id="ba979-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba979-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba979-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba979-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba979-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ba979-125">INPUTS</span></span>

### <span data-ttu-id="ba979-126">System.object</span><span class="sxs-lookup"><span data-stu-id="ba979-126">System.String</span></span>

## <span data-ttu-id="ba979-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ba979-127">OUTPUTS</span></span>

### <span data-ttu-id="ba979-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="ba979-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="ba979-129">\` \[ \[ PSSharedAccessSignatureAuthorizationRule、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ba979-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ba979-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ba979-130">NOTES</span></span>

## <span data-ttu-id="ba979-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba979-131">RELATED LINKS</span></span>

