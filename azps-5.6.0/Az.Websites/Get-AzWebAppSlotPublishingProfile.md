---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: fed1be90af7aad2126b20dbe830f5069cc62e01f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912954"
---
# <span data-ttu-id="1993f-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1993f-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="1993f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1993f-102">SYNOPSIS</span></span>
<span data-ttu-id="1993f-103">獲得 Azure Web App 插槽發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="1993f-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="1993f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1993f-104">SYNTAX</span></span>

### <span data-ttu-id="1993f-105">S1</span><span class="sxs-lookup"><span data-stu-id="1993f-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1993f-106">S2</span><span class="sxs-lookup"><span data-stu-id="1993f-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1993f-107">描述</span><span class="sxs-lookup"><span data-stu-id="1993f-107">DESCRIPTION</span></span>
<span data-ttu-id="1993f-108">**Get-AzWebAppSlotPublishingProfile** Cmdlet 會取得指定時段的 Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="1993f-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="1993f-109">例子</span><span class="sxs-lookup"><span data-stu-id="1993f-109">EXAMPLES</span></span>

### <span data-ttu-id="1993f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1993f-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1993f-111">此命令會針對與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp，以 Ftp 格式的 slot Slot001 發佈設定檔，並儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="1993f-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1993f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1993f-112">PARAMETERS</span></span>

### <span data-ttu-id="1993f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1993f-113">-DefaultProfile</span></span>
<span data-ttu-id="1993f-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1993f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1993f-115">-格式</span><span class="sxs-lookup"><span data-stu-id="1993f-115">-Format</span></span>
<span data-ttu-id="1993f-116">格式</span><span class="sxs-lookup"><span data-stu-id="1993f-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-117">-IncludeDsterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="1993f-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1993f-118">如果為 True，請包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="1993f-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1993f-119">-Name</span></span>
<span data-ttu-id="1993f-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1993f-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1993f-121">-OutputFile</span></span>
<span data-ttu-id="1993f-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="1993f-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1993f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1993f-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="1993f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="1993f-125">-Slot</span></span>
<span data-ttu-id="1993f-126">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="1993f-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1993f-127">-WebApp</span></span>
<span data-ttu-id="1993f-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="1993f-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1993f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1993f-129">CommonParameters</span></span>
<span data-ttu-id="1993f-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1993f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1993f-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1993f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1993f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1993f-132">INPUTS</span></span>

### <span data-ttu-id="1993f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1993f-133">System.String</span></span>

### <span data-ttu-id="1993f-134">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1993f-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1993f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1993f-135">OUTPUTS</span></span>

### <span data-ttu-id="1993f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1993f-136">System.String</span></span>

## <span data-ttu-id="1993f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1993f-137">NOTES</span></span>

## <span data-ttu-id="1993f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1993f-138">RELATED LINKS</span></span>

[<span data-ttu-id="1993f-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1993f-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="1993f-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1993f-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1993f-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1993f-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
