---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435713"
---
# <span data-ttu-id="14e77-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="14e77-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="14e77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14e77-102">SYNOPSIS</span></span>
<span data-ttu-id="14e77-103">**測試 AzPrivateLinkServiceVisibility** 會檢查是否可在目前使用中看到私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="14e77-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="14e77-104">句法</span><span class="sxs-lookup"><span data-stu-id="14e77-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e77-105">說明</span><span class="sxs-lookup"><span data-stu-id="14e77-105">DESCRIPTION</span></span>
<span data-ttu-id="14e77-106">檢查 [私人連結服務] 在目前使用中是否可見。</span><span class="sxs-lookup"><span data-stu-id="14e77-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="14e77-107">示例</span><span class="sxs-lookup"><span data-stu-id="14e77-107">EXAMPLES</span></span>

### <span data-ttu-id="14e77-108">範例1：檢查 contoso.cloudapp.azure.com 是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="14e77-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="14e77-109">參數</span><span class="sxs-lookup"><span data-stu-id="14e77-109">PARAMETERS</span></span>

### <span data-ttu-id="14e77-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e77-110">-DefaultProfile</span></span>
<span data-ttu-id="14e77-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14e77-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e77-112">-位置</span><span class="sxs-lookup"><span data-stu-id="14e77-112">-Location</span></span>
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

### <span data-ttu-id="14e77-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="14e77-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e77-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e77-114">-ResourceGroupName</span></span>
<span data-ttu-id="14e77-115">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14e77-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="14e77-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e77-116">CommonParameters</span></span>
<span data-ttu-id="14e77-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14e77-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e77-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14e77-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e77-119">輸入</span><span class="sxs-lookup"><span data-stu-id="14e77-119">INPUTS</span></span>

### <span data-ttu-id="14e77-120">所有</span><span class="sxs-lookup"><span data-stu-id="14e77-120">None</span></span>

## <span data-ttu-id="14e77-121">輸出</span><span class="sxs-lookup"><span data-stu-id="14e77-121">OUTPUTS</span></span>

### <span data-ttu-id="14e77-122">System.object</span><span class="sxs-lookup"><span data-stu-id="14e77-122">System.Boolean</span></span>

## <span data-ttu-id="14e77-123">筆記</span><span class="sxs-lookup"><span data-stu-id="14e77-123">NOTES</span></span>

## <span data-ttu-id="14e77-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="14e77-124">RELATED LINKS</span></span>
