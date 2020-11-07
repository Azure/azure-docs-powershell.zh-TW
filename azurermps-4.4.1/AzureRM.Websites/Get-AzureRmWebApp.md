---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624522"
---
# <span data-ttu-id="0d1a0-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="0d1a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1a0-103">在指定的資源群組中取得 Azure Web Apps。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d1a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d1a0-104">SYNTAX</span></span>

### <span data-ttu-id="0d1a0-105">S1</span><span class="sxs-lookup"><span data-stu-id="0d1a0-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d1a0-106">S2</span><span class="sxs-lookup"><span data-stu-id="0d1a0-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d1a0-107">S3</span><span class="sxs-lookup"><span data-stu-id="0d1a0-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d1a0-108">說明</span><span class="sxs-lookup"><span data-stu-id="0d1a0-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1a0-109">**AzureRmWebApp** Cmdlet 會取得 Azure Web App 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0d1a0-110">示例</span><span class="sxs-lookup"><span data-stu-id="0d1a0-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1a0-111">範例1：從資源群組取得 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="0d1a0-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="0d1a0-112">這個命令會取得屬於資源群組 Default-Web WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0d1a0-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d1a0-113">PARAMETERS</span></span>

### <span data-ttu-id="0d1a0-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0d1a0-114">-AppServicePlan</span></span>
<span data-ttu-id="0d1a0-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="0d1a0-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1a0-116">-位置</span><span class="sxs-lookup"><span data-stu-id="0d1a0-116">-Location</span></span>
<span data-ttu-id="0d1a0-117">位於</span><span class="sxs-lookup"><span data-stu-id="0d1a0-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1a0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d1a0-118">-Name</span></span>
<span data-ttu-id="0d1a0-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="0d1a0-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d1a0-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0d1a0-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1a0-122">-DefaultProfile</span></span>
<span data-ttu-id="0d1a0-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1a0-124">CommonParameters</span></span>
<span data-ttu-id="0d1a0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1a0-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d1a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1a0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0d1a0-127">INPUTS</span></span>

## <span data-ttu-id="0d1a0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0d1a0-128">OUTPUTS</span></span>

## <span data-ttu-id="0d1a0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0d1a0-129">NOTES</span></span>

## <span data-ttu-id="0d1a0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d1a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d1a0-131">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0d1a0-132">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0d1a0-133">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0d1a0-134">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0d1a0-135">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0d1a0-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


