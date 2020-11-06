---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455316"
---
# <span data-ttu-id="479ed-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="479ed-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="479ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="479ed-102">SYNOPSIS</span></span>
<span data-ttu-id="479ed-103">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="479ed-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="479ed-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="479ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="479ed-105">DESCRIPTION</span></span>
<span data-ttu-id="479ed-106">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="479ed-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="479ed-107">您可以列出所有按鍵，或依據特定的索引鍵名稱來篩選清單。</span><span class="sxs-lookup"><span data-stu-id="479ed-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="479ed-108">示例</span><span class="sxs-lookup"><span data-stu-id="479ed-108">EXAMPLES</span></span>

### <span data-ttu-id="479ed-109">範例1取得所有按鍵</span><span class="sxs-lookup"><span data-stu-id="479ed-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="479ed-110">取得名為 "myiothub" 的 IotHub 的所有鍵</span><span class="sxs-lookup"><span data-stu-id="479ed-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="479ed-111">範例2取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="479ed-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="479ed-112">取得名為「iothubowner」的名為「myiothub」之 IotHub 的索引鍵資訊</span><span class="sxs-lookup"><span data-stu-id="479ed-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="479ed-113">參數</span><span class="sxs-lookup"><span data-stu-id="479ed-113">PARAMETERS</span></span>

### <span data-ttu-id="479ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479ed-114">-DefaultProfile</span></span>
<span data-ttu-id="479ed-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="479ed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="479ed-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="479ed-116">-KeyName</span></span>
<span data-ttu-id="479ed-117">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="479ed-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479ed-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="479ed-118">-Name</span></span>
<span data-ttu-id="479ed-119">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="479ed-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="479ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="479ed-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="479ed-121">Resource Group Name</span></span>

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

### <span data-ttu-id="479ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479ed-122">CommonParameters</span></span>
<span data-ttu-id="479ed-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="479ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479ed-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="479ed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479ed-125">輸入</span><span class="sxs-lookup"><span data-stu-id="479ed-125">INPUTS</span></span>

### <span data-ttu-id="479ed-126">System.object</span><span class="sxs-lookup"><span data-stu-id="479ed-126">System.String</span></span>

## <span data-ttu-id="479ed-127">輸出</span><span class="sxs-lookup"><span data-stu-id="479ed-127">OUTPUTS</span></span>

### <span data-ttu-id="479ed-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="479ed-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="479ed-129">筆記</span><span class="sxs-lookup"><span data-stu-id="479ed-129">NOTES</span></span>

## <span data-ttu-id="479ed-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="479ed-130">RELATED LINKS</span></span>
