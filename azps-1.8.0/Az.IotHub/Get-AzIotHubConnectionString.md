---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787550"
---
# <span data-ttu-id="b872a-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="b872a-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="b872a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b872a-102">SYNOPSIS</span></span>
<span data-ttu-id="b872a-103">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="b872a-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="b872a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b872a-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b872a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b872a-105">DESCRIPTION</span></span>
<span data-ttu-id="b872a-106">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="b872a-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="b872a-107">您可以為所有的按鍵取得 connectionstrings，或使用特定的金鑰名稱進行篩選。</span><span class="sxs-lookup"><span data-stu-id="b872a-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="b872a-108">示例</span><span class="sxs-lookup"><span data-stu-id="b872a-108">EXAMPLES</span></span>

### <span data-ttu-id="b872a-109">範例1取得所有 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="b872a-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b872a-110">取得名為 "myiothub" 的 iothub 所有鍵的 connectionstrings</span><span class="sxs-lookup"><span data-stu-id="b872a-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="b872a-111">範例2取得特定金鑰的 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="b872a-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="b872a-112">針對名為 "myiothub" 的 iothub，取得名為 "mykey" 之金鑰的 connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="b872a-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="b872a-113">參數</span><span class="sxs-lookup"><span data-stu-id="b872a-113">PARAMETERS</span></span>

### <span data-ttu-id="b872a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b872a-114">-DefaultProfile</span></span>
<span data-ttu-id="b872a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b872a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b872a-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b872a-116">-KeyName</span></span>
<span data-ttu-id="b872a-117">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="b872a-117">Name of the Key</span></span>

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

### <span data-ttu-id="b872a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b872a-118">-Name</span></span>
<span data-ttu-id="b872a-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b872a-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="b872a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b872a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b872a-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b872a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b872a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b872a-122">CommonParameters</span></span>
<span data-ttu-id="b872a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b872a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b872a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b872a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b872a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b872a-125">INPUTS</span></span>

### <span data-ttu-id="b872a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b872a-126">System.String</span></span>

## <span data-ttu-id="b872a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b872a-127">OUTPUTS</span></span>

### <span data-ttu-id="b872a-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b872a-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b872a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b872a-129">NOTES</span></span>

## <span data-ttu-id="b872a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b872a-130">RELATED LINKS</span></span>
