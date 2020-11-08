---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139203"
---
# <span data-ttu-id="2914e-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2914e-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="2914e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2914e-102">SYNOPSIS</span></span>
<span data-ttu-id="2914e-103">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="2914e-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="2914e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2914e-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2914e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2914e-105">DESCRIPTION</span></span>
<span data-ttu-id="2914e-106">取得 IotHub connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="2914e-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="2914e-107">您可以為所有的按鍵取得 connectionstrings，或使用特定的金鑰名稱進行篩選。</span><span class="sxs-lookup"><span data-stu-id="2914e-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="2914e-108">示例</span><span class="sxs-lookup"><span data-stu-id="2914e-108">EXAMPLES</span></span>

### <span data-ttu-id="2914e-109">範例1取得所有 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="2914e-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2914e-110">取得名為 "myiothub" 的 iothub 所有鍵的 connectionstrings</span><span class="sxs-lookup"><span data-stu-id="2914e-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="2914e-111">範例2取得特定金鑰的 IotHub connectionstrings</span><span class="sxs-lookup"><span data-stu-id="2914e-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="2914e-112">針對名為 "myiothub" 的 iothub，取得名為 "mykey" 之金鑰的 connectionstrings。</span><span class="sxs-lookup"><span data-stu-id="2914e-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="2914e-113">參數</span><span class="sxs-lookup"><span data-stu-id="2914e-113">PARAMETERS</span></span>

### <span data-ttu-id="2914e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2914e-114">-DefaultProfile</span></span>
<span data-ttu-id="2914e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2914e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2914e-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2914e-116">-KeyName</span></span>
<span data-ttu-id="2914e-117">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="2914e-117">Name of the Key</span></span>

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

### <span data-ttu-id="2914e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2914e-118">-Name</span></span>
<span data-ttu-id="2914e-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="2914e-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="2914e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2914e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2914e-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2914e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2914e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2914e-122">CommonParameters</span></span>
<span data-ttu-id="2914e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2914e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2914e-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2914e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2914e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2914e-125">INPUTS</span></span>

### <span data-ttu-id="2914e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2914e-126">System.String</span></span>

## <span data-ttu-id="2914e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2914e-127">OUTPUTS</span></span>

### <span data-ttu-id="2914e-128">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="2914e-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="2914e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2914e-129">NOTES</span></span>

## <span data-ttu-id="2914e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2914e-130">RELATED LINKS</span></span>