---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278396"
---
# <span data-ttu-id="fb7f7-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="fb7f7-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="fb7f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7f7-103">重新產生用來存取與媒體服務相關聯之 REST 端點的金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="fb7f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb7f7-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="fb7f7-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7f7-106">**AzMediaServiceKey** Cmdlet 會重新產生一個用來存取 Representational 狀態轉移的金鑰， (與媒體服務相關聯的 REST) 端點。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="fb7f7-107">示例</span><span class="sxs-lookup"><span data-stu-id="fb7f7-107">EXAMPLES</span></span>

### <span data-ttu-id="fb7f7-108">範例1：重新產生用來存取媒體服務的主鍵</span><span class="sxs-lookup"><span data-stu-id="fb7f7-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="fb7f7-109">這個命令會重新產生屬於名為 ResourceGroup004 之資源群組之名為 MediaService001 的媒體服務的主機碼。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="fb7f7-110">範例2：重新產生存取媒體服務時所用的次要金鑰</span><span class="sxs-lookup"><span data-stu-id="fb7f7-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="fb7f7-111">這個命令會為屬於名為 Resourcegroup123 之資源群組的名為 MediaService002 的媒體服務重新產生次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="fb7f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb7f7-112">PARAMETERS</span></span>

### <span data-ttu-id="fb7f7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb7f7-113">-AccountName</span></span>
<span data-ttu-id="fb7f7-114">指定此 Cmdlet 所再生之媒體服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7f7-115">-DefaultProfile</span></span>
<span data-ttu-id="fb7f7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb7f7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7f7-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fb7f7-117">-KeyType</span></span>
<span data-ttu-id="fb7f7-118">指定媒體服務的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="fb7f7-119">此參數可接受的值為：主要或次要。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb7f7-121">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="fb7f7-122">-確認</span><span class="sxs-lookup"><span data-stu-id="fb7f7-122">-Confirm</span></span>
<span data-ttu-id="fb7f7-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7f7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7f7-124">-WhatIf</span></span>
<span data-ttu-id="fb7f7-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7f7-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7f7-127">CommonParameters</span></span>
<span data-ttu-id="fb7f7-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7f7-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb7f7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7f7-130">輸入</span><span class="sxs-lookup"><span data-stu-id="fb7f7-130">INPUTS</span></span>

### <span data-ttu-id="fb7f7-131">System.object</span><span class="sxs-lookup"><span data-stu-id="fb7f7-131">System.String</span></span>

## <span data-ttu-id="fb7f7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fb7f7-132">OUTPUTS</span></span>

### <span data-ttu-id="fb7f7-133">PSServiceKey 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb7f7-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="fb7f7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fb7f7-134">NOTES</span></span>

## <span data-ttu-id="fb7f7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb7f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="fb7f7-136">AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="fb7f7-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


