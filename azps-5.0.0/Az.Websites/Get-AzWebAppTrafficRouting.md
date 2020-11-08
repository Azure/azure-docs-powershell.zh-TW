---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138566"
---
# <span data-ttu-id="cba89-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cba89-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="cba89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cba89-102">SYNOPSIS</span></span>
<span data-ttu-id="cba89-103">針對指定的槽名稱取得路由規則。</span><span class="sxs-lookup"><span data-stu-id="cba89-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="cba89-104">句法</span><span class="sxs-lookup"><span data-stu-id="cba89-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba89-105">說明</span><span class="sxs-lookup"><span data-stu-id="cba89-105">DESCRIPTION</span></span>
<span data-ttu-id="cba89-106">**AzWebAppTrafficRouting** Cmdlet 會從 Azure Web App 槽取得路由規則配置。</span><span class="sxs-lookup"><span data-stu-id="cba89-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="cba89-107">示例</span><span class="sxs-lookup"><span data-stu-id="cba89-107">EXAMPLES</span></span>

### <span data-ttu-id="cba89-108">範例1從 webapp 槽取得特定路由規則</span><span class="sxs-lookup"><span data-stu-id="cba89-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="cba89-109">這個命令會針對特定的 webapp 槽取得路由規則。</span><span class="sxs-lookup"><span data-stu-id="cba89-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="cba89-110">參數</span><span class="sxs-lookup"><span data-stu-id="cba89-110">PARAMETERS</span></span>

### <span data-ttu-id="cba89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba89-111">-DefaultProfile</span></span>
<span data-ttu-id="cba89-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cba89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba89-113">-ResourceGroupName</span></span>
<span data-ttu-id="cba89-114">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cba89-114">Resource Group Name</span></span>

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

### <span data-ttu-id="cba89-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="cba89-115">-RuleName</span></span>
<span data-ttu-id="cba89-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="cba89-116">Rule Name</span></span>
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

### <span data-ttu-id="cba89-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="cba89-117">-WebAppName</span></span>
<span data-ttu-id="cba89-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="cba89-118">WebApp Name</span></span>

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

### <span data-ttu-id="cba89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba89-119">CommonParameters</span></span>
<span data-ttu-id="cba89-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cba89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba89-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cba89-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba89-122">輸入</span><span class="sxs-lookup"><span data-stu-id="cba89-122">INPUTS</span></span>

### <span data-ttu-id="cba89-123">所有</span><span class="sxs-lookup"><span data-stu-id="cba89-123">None</span></span>

## <span data-ttu-id="cba89-124">輸出</span><span class="sxs-lookup"><span data-stu-id="cba89-124">OUTPUTS</span></span>

### <span data-ttu-id="cba89-125">RampUpRule 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="cba89-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="cba89-126">筆記</span><span class="sxs-lookup"><span data-stu-id="cba89-126">NOTES</span></span>

## <span data-ttu-id="cba89-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cba89-127">RELATED LINKS</span></span>

[<span data-ttu-id="cba89-128">更新-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cba89-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="cba89-129">附加 AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cba89-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="cba89-130">移除-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cba89-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
