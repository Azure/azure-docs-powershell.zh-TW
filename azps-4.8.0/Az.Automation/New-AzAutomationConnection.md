---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969385"
---
# <span data-ttu-id="77db5-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="77db5-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="77db5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77db5-102">SYNOPSIS</span></span>
<span data-ttu-id="77db5-103">建立自動化連線。</span><span class="sxs-lookup"><span data-stu-id="77db5-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="77db5-104">句法</span><span class="sxs-lookup"><span data-stu-id="77db5-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77db5-105">說明</span><span class="sxs-lookup"><span data-stu-id="77db5-105">DESCRIPTION</span></span>
<span data-ttu-id="77db5-106">**新的-AzAutomationConnection** Cmdlet 會在 Azure 自動化中建立連線。</span><span class="sxs-lookup"><span data-stu-id="77db5-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="77db5-107">示例</span><span class="sxs-lookup"><span data-stu-id="77db5-107">EXAMPLES</span></span>

### <span data-ttu-id="77db5-108">範例1：建立 ConnectionTypeName = Azure 的連線</span><span class="sxs-lookup"><span data-stu-id="77db5-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="77db5-109">第一個命令會將欄位值的雜湊表指派給 $FieldValue 變數。</span><span class="sxs-lookup"><span data-stu-id="77db5-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="77db5-110">第二個命令會在名為 AutomationAccount01 的自動化帳戶中，建立名為 Connection12 的 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="77db5-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="77db5-111">命令在 $FieldValues 中使用連接欄位的值。</span><span class="sxs-lookup"><span data-stu-id="77db5-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="77db5-112">範例2：建立 ConnectionTypeName = AzureServicePrincipal 的連接</span><span class="sxs-lookup"><span data-stu-id="77db5-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="77db5-113">此命令會在使用 $RunAsAccountConnectionFieldValues 和 ConnectionTypeName = AzureServicePrincipal 的自動化帳戶（名為 AutomationAccount01）中建立名為 Connection13 的 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="77db5-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="77db5-114">此 ConnectionTypeName = AzureServicePrincipal 主要用於 Azure Run As 帳戶。</span><span class="sxs-lookup"><span data-stu-id="77db5-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="77db5-115">範例3：建立 ConnectionTypeName = AzureClassicCertificate 的連接</span><span class="sxs-lookup"><span data-stu-id="77db5-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="77db5-116">此命令會在使用 $ClassicRunAsAccountConnectionFieldValues 和 ConnectionTypeName = AzureClassicCertificate 的自動化帳戶（名為 AutomationAccount01）中建立名為 Connection14 的 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="77db5-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="77db5-117">此 ConnectionTypeName = AzureClassicCertificate 主要用於 Azure 傳統運行方式帳戶。</span><span class="sxs-lookup"><span data-stu-id="77db5-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="77db5-118">參數</span><span class="sxs-lookup"><span data-stu-id="77db5-118">PARAMETERS</span></span>

### <span data-ttu-id="77db5-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77db5-119">-AutomationAccountName</span></span>
<span data-ttu-id="77db5-120">指定此 Cmdlet 建立連線之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="77db5-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="77db5-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="77db5-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="77db5-122">指定包含鍵/值對的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="77db5-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="77db5-123">鍵代表指定連線類型的連接欄位。</span><span class="sxs-lookup"><span data-stu-id="77db5-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="77db5-124">這些值代表連接實例之每個連接欄位的特定值。</span><span class="sxs-lookup"><span data-stu-id="77db5-124">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77db5-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="77db5-125">-ConnectionTypeName</span></span>
<span data-ttu-id="77db5-126">指定連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="77db5-126">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77db5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77db5-127">-DefaultProfile</span></span>
<span data-ttu-id="77db5-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="77db5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77db5-129">-描述</span><span class="sxs-lookup"><span data-stu-id="77db5-129">-Description</span></span>
<span data-ttu-id="77db5-130">指定連線的描述。</span><span class="sxs-lookup"><span data-stu-id="77db5-130">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77db5-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="77db5-131">-Name</span></span>
<span data-ttu-id="77db5-132">指定連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="77db5-132">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77db5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77db5-133">-ResourceGroupName</span></span>
<span data-ttu-id="77db5-134">指定此 Cmdlet 建立連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77db5-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="77db5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77db5-135">CommonParameters</span></span>
<span data-ttu-id="77db5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77db5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77db5-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77db5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77db5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="77db5-138">INPUTS</span></span>

### <span data-ttu-id="77db5-139">System.object</span><span class="sxs-lookup"><span data-stu-id="77db5-139">System.String</span></span>

### <span data-ttu-id="77db5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="77db5-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="77db5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="77db5-141">OUTPUTS</span></span>

### <span data-ttu-id="77db5-142">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="77db5-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="77db5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="77db5-143">NOTES</span></span>

## <span data-ttu-id="77db5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="77db5-144">RELATED LINKS</span></span>

[<span data-ttu-id="77db5-145">AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="77db5-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="77db5-146">移除-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="77db5-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


