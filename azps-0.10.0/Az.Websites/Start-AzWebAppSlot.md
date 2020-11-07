---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794939"
---
# <span data-ttu-id="f5999-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="f5999-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5999-102">SYNOPSIS</span></span>
<span data-ttu-id="f5999-103">啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="f5999-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="f5999-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5999-104">SYNTAX</span></span>

### <span data-ttu-id="f5999-105">S1</span><span class="sxs-lookup"><span data-stu-id="f5999-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5999-106">S2</span><span class="sxs-lookup"><span data-stu-id="f5999-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5999-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5999-107">DESCRIPTION</span></span>
<span data-ttu-id="f5999-108">**AzWebAppSlot** Cmdlet 會啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="f5999-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="f5999-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5999-109">EXAMPLES</span></span>

### <span data-ttu-id="f5999-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f5999-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="f5999-111">這個命令會啟動一個名為 Slot001 的槽，該槽屬於名為 [Default-Web-WestUS] 的資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="f5999-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f5999-112">參數</span><span class="sxs-lookup"><span data-stu-id="f5999-112">PARAMETERS</span></span>

### <span data-ttu-id="f5999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5999-113">-DefaultProfile</span></span>
<span data-ttu-id="f5999-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5999-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5999-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5999-115">-Name</span></span>
<span data-ttu-id="f5999-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f5999-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5999-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5999-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5999-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f5999-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5999-119">-槽</span><span class="sxs-lookup"><span data-stu-id="f5999-119">-Slot</span></span>
<span data-ttu-id="f5999-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="f5999-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5999-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f5999-121">-WebApp</span></span>
<span data-ttu-id="f5999-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f5999-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5999-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5999-123">CommonParameters</span></span>
<span data-ttu-id="f5999-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5999-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5999-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5999-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5999-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f5999-126">INPUTS</span></span>

### <span data-ttu-id="f5999-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="f5999-127">Site</span></span>
<span data-ttu-id="f5999-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f5999-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f5999-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f5999-129">OUTPUTS</span></span>

## <span data-ttu-id="f5999-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f5999-130">NOTES</span></span>

## <span data-ttu-id="f5999-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5999-131">RELATED LINKS</span></span>

[<span data-ttu-id="f5999-132">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f5999-133">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="f5999-134">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f5999-135">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f5999-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f5999-137">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5999-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f5999-138">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5999-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
