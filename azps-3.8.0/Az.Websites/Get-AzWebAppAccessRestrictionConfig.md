---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797410"
---
# <span data-ttu-id="1cdb4-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1cdb4-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="1cdb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cdb4-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdb4-103">取得 Azure Web App 的存取 Restiction 設定。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="1cdb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cdb4-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cdb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="1cdb4-105">DESCRIPTION</span></span>
<span data-ttu-id="1cdb4-106">**AzWebAppAccessRestrictionConfig** Cmdlet 會取得有關 Azure Web App 的存取限制配置。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="1cdb4-107">示例</span><span class="sxs-lookup"><span data-stu-id="1cdb4-107">EXAMPLES</span></span>

### <span data-ttu-id="1cdb4-108">範例1：從資源群組取得 Web 應用程式存取限制配置</span><span class="sxs-lookup"><span data-stu-id="1cdb4-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1cdb4-109">這個命令會取得一個名為 ContosoSite 的 Web App 的存取限制配置，該應用程式屬於資源群組預設-Web-WestUS。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1cdb4-110">參數</span><span class="sxs-lookup"><span data-stu-id="1cdb4-110">PARAMETERS</span></span>

### <span data-ttu-id="1cdb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdb4-111">-DefaultProfile</span></span>
<span data-ttu-id="1cdb4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cdb4-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cdb4-113">-Name</span></span>
<span data-ttu-id="1cdb4-114">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1cdb4-114">WebApp Name</span></span>

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

### <span data-ttu-id="1cdb4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cdb4-115">-ResourceGroupName</span></span>
<span data-ttu-id="1cdb4-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1cdb4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1cdb4-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="1cdb4-117">-SlotName</span></span>
<span data-ttu-id="1cdb4-118">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="1cdb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdb4-119">CommonParameters</span></span>
<span data-ttu-id="1cdb4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdb4-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdb4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1cdb4-122">INPUTS</span></span>

### <span data-ttu-id="1cdb4-123">System.object</span><span class="sxs-lookup"><span data-stu-id="1cdb4-123">System.String</span></span>

## <span data-ttu-id="1cdb4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1cdb4-124">OUTPUTS</span></span>

### <span data-ttu-id="1cdb4-125">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="1cdb4-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="1cdb4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1cdb4-126">NOTES</span></span>

## <span data-ttu-id="1cdb4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cdb4-127">RELATED LINKS</span></span>

[<span data-ttu-id="1cdb4-128">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1cdb4-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="1cdb4-129">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1cdb4-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="1cdb4-130">移除-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1cdb4-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)