---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911085"
---
# <span data-ttu-id="6dfc0-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="6dfc0-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="6dfc0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6dfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfc0-103">獲得 IotHub 連接字串。</span><span class="sxs-lookup"><span data-stu-id="6dfc0-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="6dfc0-104">語法</span><span class="sxs-lookup"><span data-stu-id="6dfc0-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dfc0-105">描述</span><span class="sxs-lookup"><span data-stu-id="6dfc0-105">DESCRIPTION</span></span>
<span data-ttu-id="6dfc0-106">獲得 IotHub 連接字串。</span><span class="sxs-lookup"><span data-stu-id="6dfc0-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="6dfc0-107">您可以取得所有按鍵的連接字串，或根據特定金鑰名稱進行篩選。</span><span class="sxs-lookup"><span data-stu-id="6dfc0-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="6dfc0-108">例子</span><span class="sxs-lookup"><span data-stu-id="6dfc0-108">EXAMPLES</span></span>

### <span data-ttu-id="6dfc0-109">範例 1 取得所有 IotHub 連接字串</span><span class="sxs-lookup"><span data-stu-id="6dfc0-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6dfc0-110">為名為「myiothub」的 iothub 所有按鍵獲得連接字串</span><span class="sxs-lookup"><span data-stu-id="6dfc0-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="6dfc0-111">範例 2 取得特定金鑰的 IotHub 連接字串</span><span class="sxs-lookup"><span data-stu-id="6dfc0-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="6dfc0-112">為名為 "myiothub" 的 iothub，獲得名稱為 "mykey" 的金鑰之連接字串</span><span class="sxs-lookup"><span data-stu-id="6dfc0-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="6dfc0-113">參數</span><span class="sxs-lookup"><span data-stu-id="6dfc0-113">PARAMETERS</span></span>

### <span data-ttu-id="6dfc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfc0-114">-DefaultProfile</span></span>
<span data-ttu-id="6dfc0-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6dfc0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dfc0-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6dfc0-116">-KeyName</span></span>
<span data-ttu-id="6dfc0-117">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="6dfc0-117">Name of the Key</span></span>

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

### <span data-ttu-id="6dfc0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6dfc0-118">-Name</span></span>
<span data-ttu-id="6dfc0-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="6dfc0-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="6dfc0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfc0-120">-ResourceGroupName</span></span>
<span data-ttu-id="6dfc0-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="6dfc0-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6dfc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfc0-122">CommonParameters</span></span>
<span data-ttu-id="6dfc0-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6dfc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfc0-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6dfc0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfc0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6dfc0-125">INPUTS</span></span>

### <span data-ttu-id="6dfc0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6dfc0-126">System.String</span></span>

## <span data-ttu-id="6dfc0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6dfc0-127">OUTPUTS</span></span>

### <span data-ttu-id="6dfc0-128">Microsoft.Azure.Commands.management.IotHub.models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6dfc0-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="6dfc0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6dfc0-129">NOTES</span></span>

## <span data-ttu-id="6dfc0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dfc0-130">RELATED LINKS</span></span>
