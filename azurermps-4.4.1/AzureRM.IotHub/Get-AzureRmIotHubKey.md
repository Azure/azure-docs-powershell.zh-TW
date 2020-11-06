---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453480"
---
# <span data-ttu-id="2aa95-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="2aa95-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="2aa95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2aa95-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa95-103">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="2aa95-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aa95-104">句法</span><span class="sxs-lookup"><span data-stu-id="2aa95-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aa95-105">說明</span><span class="sxs-lookup"><span data-stu-id="2aa95-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa95-106">取得 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="2aa95-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="2aa95-107">您可以列出所有按鍵，或依據特定的索引鍵名稱來篩選清單。</span><span class="sxs-lookup"><span data-stu-id="2aa95-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="2aa95-108">示例</span><span class="sxs-lookup"><span data-stu-id="2aa95-108">EXAMPLES</span></span>

### <span data-ttu-id="2aa95-109">範例1取得所有按鍵</span><span class="sxs-lookup"><span data-stu-id="2aa95-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2aa95-110">取得名為 "myiothub" 的 IotHub 的所有鍵</span><span class="sxs-lookup"><span data-stu-id="2aa95-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2aa95-111">範例2取得特定金鑰的資訊</span><span class="sxs-lookup"><span data-stu-id="2aa95-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="2aa95-112">取得名為「iothubowner」的名為「myiothub」之 IotHub 的索引鍵資訊</span><span class="sxs-lookup"><span data-stu-id="2aa95-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2aa95-113">參數</span><span class="sxs-lookup"><span data-stu-id="2aa95-113">PARAMETERS</span></span>

### <span data-ttu-id="2aa95-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2aa95-114">-KeyName</span></span>
<span data-ttu-id="2aa95-115">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="2aa95-115">Name of the Key</span></span>

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

### <span data-ttu-id="2aa95-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2aa95-116">-Name</span></span>
<span data-ttu-id="2aa95-117">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="2aa95-117">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2aa95-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa95-118">-ResourceGroupName</span></span>
<span data-ttu-id="2aa95-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2aa95-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2aa95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa95-120">-DefaultProfile</span></span>
<span data-ttu-id="2aa95-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2aa95-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aa95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa95-122">CommonParameters</span></span>
<span data-ttu-id="2aa95-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2aa95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa95-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2aa95-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa95-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2aa95-125">INPUTS</span></span>

### <span data-ttu-id="2aa95-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2aa95-126">System.String</span></span>

## <span data-ttu-id="2aa95-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2aa95-127">OUTPUTS</span></span>

### <span data-ttu-id="2aa95-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="2aa95-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="2aa95-129">\` \[ \[ PSSharedAccessSignatureAuthorizationRule、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="2aa95-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="2aa95-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2aa95-130">NOTES</span></span>

## <span data-ttu-id="2aa95-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2aa95-131">RELATED LINKS</span></span>

