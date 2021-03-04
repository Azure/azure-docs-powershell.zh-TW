---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901702"
---
# <span data-ttu-id="1f59c-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1f59c-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="1f59c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f59c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f59c-103">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="1f59c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f59c-104">SYNTAX</span></span>

### <span data-ttu-id="1f59c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f59c-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f59c-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f59c-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f59c-107">描述</span><span class="sxs-lookup"><span data-stu-id="1f59c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f59c-108">**Set-AzNotificationHub** Cmdlet 會修改通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="1f59c-109">您可以用兩種方式修改通知中樞屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="1f59c-110">例如，您可以建立 **NotificationHubAttributes** 物件的實例，然後將該物件設定為您想要新中樞擁有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="1f59c-111">這可透過 .NET Framework 完成。</span><span class="sxs-lookup"><span data-stu-id="1f59c-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="1f59c-112">接著，您可以透過 *NotificationHubObj* 參數，將那些屬性值複製到中樞。</span><span class="sxs-lookup"><span data-stu-id="1f59c-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="1f59c-113">或者，您可以建立包含相關 (的 JSON (JavaScript 物件標記法) 檔案，然後透過 *InputFile* 參數來使用這些值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="1f59c-114">JSON 檔案是使用類似下列語法的文字檔： {</span><span class="sxs-lookup"><span data-stu-id="1f59c-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="1f59c-115">"Name"： "ContosoNotificationHub"，</span><span class="sxs-lookup"><span data-stu-id="1f59c-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="1f59c-116">"Location"： "West US"，</span><span class="sxs-lookup"><span data-stu-id="1f59c-116">"Location": "West US",</span></span>  
<span data-ttu-id="1f59c-117">} 與 **Set-AzNotificationHub** Cmdlet 一起使用時，上述 JSON 範例會將名為 ContosoNotificationHub 的通知中樞位置值設為美國西部。</span><span class="sxs-lookup"><span data-stu-id="1f59c-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="1f59c-118">例子</span><span class="sxs-lookup"><span data-stu-id="1f59c-118">EXAMPLES</span></span>

### <span data-ttu-id="1f59c-119">範例 1：修改通知中樞的屬性值</span><span class="sxs-lookup"><span data-stu-id="1f59c-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="1f59c-120">此命令會修改 ContosoNamespace 命名空間中通知中樞的屬性值，並將它指派給資源群組 ContosoNotificationsGroup。</span><span class="sxs-lookup"><span data-stu-id="1f59c-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="1f59c-121">命令中未指定屬性值，以及要修改的中樞名稱。</span><span class="sxs-lookup"><span data-stu-id="1f59c-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="1f59c-122">該資訊反而會包含在您C:\Configuration\Hubs.js檔案中。</span><span class="sxs-lookup"><span data-stu-id="1f59c-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="1f59c-123">範例 2</span><span class="sxs-lookup"><span data-stu-id="1f59c-123">Example 2</span></span>

<span data-ttu-id="1f59c-124">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f59c-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="1f59c-125"> (自動) </span><span class="sxs-lookup"><span data-stu-id="1f59c-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="1f59c-126">參數</span><span class="sxs-lookup"><span data-stu-id="1f59c-126">PARAMETERS</span></span>

### <span data-ttu-id="1f59c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f59c-127">-DefaultProfile</span></span>
<span data-ttu-id="1f59c-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1f59c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f59c-129">-強制</span><span class="sxs-lookup"><span data-stu-id="1f59c-129">-Force</span></span>
<span data-ttu-id="1f59c-130">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="1f59c-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f59c-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1f59c-131">-InputFile</span></span>
<span data-ttu-id="1f59c-132">指定包含通知中樞之組程資訊之 JSON 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1f59c-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f59c-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1f59c-133">-Namespace</span></span>
<span data-ttu-id="1f59c-134">指定指派通知中樞的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1f59c-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="1f59c-135">命名空間提供將通知中樞分組和分類的方式。</span><span class="sxs-lookup"><span data-stu-id="1f59c-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1f59c-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="1f59c-136">-NotificationHubObj</span></span>
<span data-ttu-id="1f59c-137">指定 **NotificationHubAttributes 物件** ，該物件包含此 Cmdlet 所修改之中樞的組配置資訊。</span><span class="sxs-lookup"><span data-stu-id="1f59c-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f59c-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f59c-138">-ResourceGroup</span></span>
<span data-ttu-id="1f59c-139">指定指派通知中樞給的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f59c-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="1f59c-140">資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。</span><span class="sxs-lookup"><span data-stu-id="1f59c-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1f59c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="1f59c-141">-Confirm</span></span>
<span data-ttu-id="1f59c-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f59c-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f59c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f59c-143">-WhatIf</span></span>
<span data-ttu-id="1f59c-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f59c-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f59c-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f59c-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f59c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f59c-146">CommonParameters</span></span>
<span data-ttu-id="1f59c-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f59c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f59c-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1f59c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f59c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1f59c-149">INPUTS</span></span>

### <span data-ttu-id="1f59c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1f59c-150">System.String</span></span>

## <span data-ttu-id="1f59c-151">輸出</span><span class="sxs-lookup"><span data-stu-id="1f59c-151">OUTPUTS</span></span>

### <span data-ttu-id="1f59c-152">Microsoft.Azure.Commands.NotificationHubs.models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1f59c-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="1f59c-153">筆記</span><span class="sxs-lookup"><span data-stu-id="1f59c-153">NOTES</span></span>

## <span data-ttu-id="1f59c-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f59c-154">RELATED LINKS</span></span>

[<span data-ttu-id="1f59c-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1f59c-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="1f59c-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1f59c-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="1f59c-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1f59c-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


