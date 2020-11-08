---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141413"
---
# <span data-ttu-id="113f4-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="113f4-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="113f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="113f4-102">SYNOPSIS</span></span>
<span data-ttu-id="113f4-103">取得可與自動核准的私人端點連結的私人連結服務識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="113f4-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="113f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="113f4-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="113f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="113f4-105">DESCRIPTION</span></span>
<span data-ttu-id="113f4-106">**AzAutoApprovedPrivateLinkService** 會取得私有連結服務識別碼的陣列，以自動核准的方式連結到私人端點。</span><span class="sxs-lookup"><span data-stu-id="113f4-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="113f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="113f4-107">EXAMPLES</span></span>

### <span data-ttu-id="113f4-108">範例</span><span class="sxs-lookup"><span data-stu-id="113f4-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="113f4-109">這個範例會傳回一個私有連結服務識別碼陣列，該陣列可連結至具有自動核准的私人端點。</span><span class="sxs-lookup"><span data-stu-id="113f4-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="113f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="113f4-110">PARAMETERS</span></span>

### <span data-ttu-id="113f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113f4-111">-DefaultProfile</span></span>
<span data-ttu-id="113f4-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="113f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="113f4-113">-位置</span><span class="sxs-lookup"><span data-stu-id="113f4-113">-Location</span></span>
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

### <span data-ttu-id="113f4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113f4-114">-ResourceGroupName</span></span>
<span data-ttu-id="113f4-115">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="113f4-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113f4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113f4-116">CommonParameters</span></span>
<span data-ttu-id="113f4-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="113f4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113f4-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="113f4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113f4-119">輸入</span><span class="sxs-lookup"><span data-stu-id="113f4-119">INPUTS</span></span>

### <span data-ttu-id="113f4-120">所有</span><span class="sxs-lookup"><span data-stu-id="113f4-120">None</span></span>

## <span data-ttu-id="113f4-121">輸出</span><span class="sxs-lookup"><span data-stu-id="113f4-121">OUTPUTS</span></span>

### <span data-ttu-id="113f4-122">PSAutoApprovedPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="113f4-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="113f4-123">筆記</span><span class="sxs-lookup"><span data-stu-id="113f4-123">NOTES</span></span>

## <span data-ttu-id="113f4-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="113f4-124">RELATED LINKS</span></span>