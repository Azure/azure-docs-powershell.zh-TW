---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907017"
---
# <span data-ttu-id="94f87-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="94f87-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="94f87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94f87-102">SYNOPSIS</span></span>

## <span data-ttu-id="94f87-103">語法</span><span class="sxs-lookup"><span data-stu-id="94f87-103">SYNTAX</span></span>

### <span data-ttu-id="94f87-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="94f87-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f87-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="94f87-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f87-106">描述</span><span class="sxs-lookup"><span data-stu-id="94f87-106">DESCRIPTION</span></span>
<span data-ttu-id="94f87-107">**Get-AzWebAppBackupList** Cmdlet 會取得 Azure Web App 的備份清單。</span><span class="sxs-lookup"><span data-stu-id="94f87-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="94f87-108">例子</span><span class="sxs-lookup"><span data-stu-id="94f87-108">EXAMPLES</span></span>

### <span data-ttu-id="94f87-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="94f87-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="94f87-110">此命令會返回與資源群組 ContosoResourceGroup 相關聯的 WebApp WebAppStandard 備份清單。</span><span class="sxs-lookup"><span data-stu-id="94f87-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="94f87-111">參數</span><span class="sxs-lookup"><span data-stu-id="94f87-111">PARAMETERS</span></span>

### <span data-ttu-id="94f87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f87-112">-DefaultProfile</span></span>
<span data-ttu-id="94f87-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f87-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f87-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="94f87-114">-Name</span></span>
<span data-ttu-id="94f87-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="94f87-115">WebApp Name</span></span>

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

### <span data-ttu-id="94f87-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f87-116">-ResourceGroupName</span></span>
<span data-ttu-id="94f87-117">資源組名</span><span class="sxs-lookup"><span data-stu-id="94f87-117">Resource Group Name</span></span>

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

### <span data-ttu-id="94f87-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="94f87-118">-Slot</span></span>
<span data-ttu-id="94f87-119">插槽名稱</span><span class="sxs-lookup"><span data-stu-id="94f87-119">Slot name</span></span>

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

### <span data-ttu-id="94f87-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="94f87-120">-WebApp</span></span>
<span data-ttu-id="94f87-121">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="94f87-121">Piped WebApp</span></span>

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

### <span data-ttu-id="94f87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f87-122">CommonParameters</span></span>
<span data-ttu-id="94f87-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94f87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f87-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="94f87-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f87-125">輸入</span><span class="sxs-lookup"><span data-stu-id="94f87-125">INPUTS</span></span>

### <span data-ttu-id="94f87-126">System.String</span><span class="sxs-lookup"><span data-stu-id="94f87-126">System.String</span></span>

### <span data-ttu-id="94f87-127">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="94f87-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="94f87-128">輸出</span><span class="sxs-lookup"><span data-stu-id="94f87-128">OUTPUTS</span></span>

### <span data-ttu-id="94f87-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="94f87-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="94f87-130">筆記</span><span class="sxs-lookup"><span data-stu-id="94f87-130">NOTES</span></span>

## <span data-ttu-id="94f87-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f87-131">RELATED LINKS</span></span>
