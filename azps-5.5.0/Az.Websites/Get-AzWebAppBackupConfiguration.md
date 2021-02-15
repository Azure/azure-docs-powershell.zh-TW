---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142806"
---
# <span data-ttu-id="61232-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="61232-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="61232-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61232-102">SYNOPSIS</span></span>

## <span data-ttu-id="61232-103">句法</span><span class="sxs-lookup"><span data-stu-id="61232-103">SYNTAX</span></span>

### <span data-ttu-id="61232-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="61232-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61232-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="61232-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61232-106">說明</span><span class="sxs-lookup"><span data-stu-id="61232-106">DESCRIPTION</span></span>
<span data-ttu-id="61232-107">**AzWebAppBackupConfiguration** Cmdlet 會取得 Azure Web App 的備份設定。</span><span class="sxs-lookup"><span data-stu-id="61232-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="61232-108">示例</span><span class="sxs-lookup"><span data-stu-id="61232-108">EXAMPLES</span></span>

### <span data-ttu-id="61232-109">範例1</span><span class="sxs-lookup"><span data-stu-id="61232-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="61232-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為 WebAppStandard 的 Web App 取得備份配置。</span><span class="sxs-lookup"><span data-stu-id="61232-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="61232-111">參數</span><span class="sxs-lookup"><span data-stu-id="61232-111">PARAMETERS</span></span>

### <span data-ttu-id="61232-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61232-112">-DefaultProfile</span></span>
<span data-ttu-id="61232-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61232-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61232-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="61232-114">-Name</span></span>
<span data-ttu-id="61232-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="61232-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61232-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61232-116">-ResourceGroupName</span></span>
<span data-ttu-id="61232-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="61232-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61232-118">-槽</span><span class="sxs-lookup"><span data-stu-id="61232-118">-Slot</span></span>
<span data-ttu-id="61232-119">槽名稱</span><span class="sxs-lookup"><span data-stu-id="61232-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61232-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="61232-120">-WebApp</span></span>
<span data-ttu-id="61232-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="61232-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61232-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61232-122">CommonParameters</span></span>
<span data-ttu-id="61232-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61232-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61232-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61232-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61232-125">輸入</span><span class="sxs-lookup"><span data-stu-id="61232-125">INPUTS</span></span>

### <span data-ttu-id="61232-126">System.object</span><span class="sxs-lookup"><span data-stu-id="61232-126">System.String</span></span>

### <span data-ttu-id="61232-127">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="61232-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="61232-128">輸出</span><span class="sxs-lookup"><span data-stu-id="61232-128">OUTPUTS</span></span>

### <span data-ttu-id="61232-129">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="61232-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="61232-130">筆記</span><span class="sxs-lookup"><span data-stu-id="61232-130">NOTES</span></span>

## <span data-ttu-id="61232-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="61232-131">RELATED LINKS</span></span>
