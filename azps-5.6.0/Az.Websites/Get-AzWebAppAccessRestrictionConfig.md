---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909881"
---
# <span data-ttu-id="3c563-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3c563-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="3c563-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c563-102">SYNOPSIS</span></span>
<span data-ttu-id="3c563-103">取得 Azure Web App 的 Access Restiction 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3c563-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="3c563-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c563-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c563-105">描述</span><span class="sxs-lookup"><span data-stu-id="3c563-105">DESCRIPTION</span></span>
<span data-ttu-id="3c563-106">**Get-AzWebAppAccessRestrictionConfig** Cmdlet 會取得 Azure Web App 的存取限制設定檔。</span><span class="sxs-lookup"><span data-stu-id="3c563-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="3c563-107">例子</span><span class="sxs-lookup"><span data-stu-id="3c563-107">EXAMPLES</span></span>

### <span data-ttu-id="3c563-108">範例 1：從資源群組取得 Web App 存取限制 Config</span><span class="sxs-lookup"><span data-stu-id="3c563-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3c563-109">此命令會取得屬於資源群組 Default-Web-WestUS 的名為 ContosoSite 的 Web App 存取限制設定檔。</span><span class="sxs-lookup"><span data-stu-id="3c563-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3c563-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c563-110">PARAMETERS</span></span>

### <span data-ttu-id="3c563-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c563-111">-DefaultProfile</span></span>
<span data-ttu-id="3c563-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c563-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c563-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c563-113">-Name</span></span>
<span data-ttu-id="3c563-114">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3c563-114">WebApp Name</span></span>

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

### <span data-ttu-id="3c563-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c563-115">-ResourceGroupName</span></span>
<span data-ttu-id="3c563-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="3c563-116">Resource Group Name</span></span>

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

### <span data-ttu-id="3c563-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="3c563-117">-SlotName</span></span>
<span data-ttu-id="3c563-118">部署插槽名稱。</span><span class="sxs-lookup"><span data-stu-id="3c563-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="3c563-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c563-119">CommonParameters</span></span>
<span data-ttu-id="3c563-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c563-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c563-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c563-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c563-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3c563-122">INPUTS</span></span>

### <span data-ttu-id="3c563-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3c563-123">System.String</span></span>

## <span data-ttu-id="3c563-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3c563-124">OUTPUTS</span></span>

### <span data-ttu-id="3c563-125">Microsoft.Azure.Commands.WebApps.models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3c563-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="3c563-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3c563-126">NOTES</span></span>

## <span data-ttu-id="3c563-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c563-127">RELATED LINKS</span></span>

[<span data-ttu-id="3c563-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3c563-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3c563-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3c563-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="3c563-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3c563-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
